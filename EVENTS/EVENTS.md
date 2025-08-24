<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Course Calendar</title>
  <!-- FullCalendar v6 from CDN -->
  <link href="https://cdn.jsdelivr.net/npm/@fullcalendar/core@6.1.15/index.global.min.css" rel="stylesheet" />
  <script src="https://cdn.jsdelivr.net/npm/@fullcalendar/core@6.1.15/index.global.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@fullcalendar/daygrid@6.1.15/index.global.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@fullcalendar/timegrid@6.1.15/index.global.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@fullcalendar/list@6.1.15/index.global.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@fullcalendar/interaction@6.1.15/index.global.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@fullcalendar/icalendar@6.1.15/index.global.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@fullcalendar/bootstrap5@6.1.15/index.global.min.js"></script>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" />
  <style>
    :root{--bg:#0b0d10;--card:#11151a;--muted:#6b7280}
    body{font-family:system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif; margin:0; background:#0b0d10; color:#f3f4f6}
    header{padding:1rem 1.25rem; border-bottom:1px solid #1f2937; position:sticky; top:0; backdrop-filter:saturate(140%) blur(6px); background:rgba(11,13,16,.8)}
    h1{font-size:1.1rem; margin:0}
    .wrap{max-width:1100px; margin:0 auto; padding:1rem}
    .card{background:#11151a; border:1px solid #1f2937; border-radius:1rem; padding:1rem}
    #calendar{padding: .5rem}
    .fc .fc-button{border-radius:.6rem; border:none}
    .fc .fc-toolbar-title{font-size:1.2rem}
    .hint{font-size:.9rem; color:#9ca3af}
    a{color:#93c5fd}
    code{background:#0b1220; padding:.1rem .35rem; border-radius:.3rem}
  </style>
  <!--
  =====================================
  Course Calendar for GitHub Pages
  =====================================
  HOW TO USE (quick):
  1) Put this file in your repo (e.g., at the root or in /docs). If using GitHub Pages, point Pages to that folder.
  2) Choose one of the event sources below and commit the corresponding file:
     • JSON:   create events.json in the same folder as this file (see template below).
     • iCal:   create events.ics (exported from Google Calendar/Outlook/etc.).
  3) Push to GitHub. Open the page on GitHub Pages (or the raw HTML via the repo's file view).
  4) Edit events.json or events.ics to update your course schedule; just commit changes.

  JSON TEMPLATE (events.json):
  [
    {
      "title": "Lecture 1: Intro",
      "start": "2025-09-22T10:30:00",
      "end":   "2025-09-22T12:00:00",
      "location": "Room 101",
      "url": "https://your-lms-link.example",
      "description": "Syllabus, grading, logistics."
    },
    {
      "title": "Lab 1",
      "start": "2025-09-24T15:00:00",
      "end":   "2025-09-24T17:00:00",
      "location": "Lab A",
      "description": "Intro to Python."
    }
  ]

  NOTES:
  - Times are ISO8601 and assumed local to the calendar's timeZone (configured below).
  - You can use all FullCalendar event fields (e.g., recurring with RRULE via rrule plugin, but not included here by default).
  - iCal source (events.ics) will be used if present; otherwise JSON; if neither, fallback to inline SAMPLE_EVENTS.
  - To customize locale/timezone, tweak the "calendar" initialization in the script.
  - This is read-only on GitHub Pages; to add/edit events you commit changes to files.
  -->
</head>
<body>
  <header>
    <div class="wrap d-flex align-items-center justify-content-between">
      <h1>📅 Course Calendar</h1>
      <div class="hint">Edit <code>events.json</code> or <code>events.ics</code> in this repo to update.</div>
    </div>
  </header>

  <main class="wrap">
    <div class="card mb-3">
      <div class="d-flex flex-wrap gap-2 align-items-center justify-content-between">
        <div>
          <strong>Views:</strong>
          <button class="btn btn-sm btn-outline-light" data-view="dayGridMonth">Month</button>
          <button class="btn btn-sm btn-outline-light" data-view="timeGridWeek">Week</button>
          <button class="btn btn-sm btn-outline-light" data-view="listMonth">Agenda</button>
        </div>
        <div>
          <label class="me-2">Timezone:</label>
          <select id="tz" class="form-select form-select-sm d-inline-block" style="width: auto">
            <option value="local">Local</option>
            <option value="Europe/Istanbul" selected>Europe/Istanbul</option>
            <option value="UTC">UTC</option>
          </select>
        </div>
      </div>
    </div>

    <div id="calendar" class="card"></div>

    <p class="hint mt-3">Tip: prefer <code>events.ics</code> if you want to manage events in Google Calendar/Outlook and just export an ICS into the repo.
      Prefer <code>events.json</code> if you want to keep everything in Git.</p>
  </main>

  <script>
    // Fallback sample events (used only if no events.json or events.ics are found)
    const SAMPLE_EVENTS = [
      {
        title: "Sample: Lecture 1",
        start: "2025-09-15T10:30:00",
        end:   "2025-09-15T12:00:00",
        location: "Room 101",
        description: "Replace this by creating events.json or events.ics",
      },
      {
        title: "Sample: Office Hours",
        start: "2025-09-16T14:00:00",
        end:   "2025-09-16T16:00:00",
        location: "Bldg A, 2nd floor",
      }
    ];

    // Render an event popover/tooltip content
    function eventContent(arg){
      // Use default text; we could customize further if needed
      return { html: `<div><strong>${arg.event.title}</strong></div>` };
    }

    function buildEventDidMount(info){
      const loc = info.event.extendedProps.location;
      const desc = info.event.extendedProps.description;
      if(loc || desc){
        info.el.title = [loc ? `Location: ${loc}` : null, desc ? desc : null].filter(Boolean).join("\n");
      }
    }

    // Try to detect which source files exist in the same directory as this HTML
    async function detectSources(){
      const base = new URL('.', window.location.href).href;
      const tryHead = async (file) => {
        try {
          const res = await fetch(base + file, { method: 'HEAD', cache: 'no-store' });
          return res.ok;
        } catch { return false; }
      };
      const hasICS = await tryHead('events.ics');
      const hasJSON = await tryHead('events.json');
      return { hasICS, hasJSON, base };
    }

    function makeCalendar(timeZone){
      const calendarEl = document.getElementById('calendar');
      const calendar = new FullCalendar.Calendar(calendarEl, {
        themeSystem: 'bootstrap5',
        initialView: 'dayGridMonth',
        height: 'auto',
        nowIndicator: true,
        eventContent,
        eventDidMount: buildEventDidMount,
        headerToolbar: {
          left: 'prev,next today',
          center: 'title',
          right: 'dayGridMonth,timeGridWeek,listMonth'
        },
        buttonText: { today: 'Today', month: 'Month', week: 'Week', day: 'Day', list: 'Agenda' },
        timeZone,
        firstDay: 1, // Monday
        slotMinTime: '08:00:00',
        slotMaxTime: '22:00:00',
        displayEventTime: true,
        eventSources: [],
      });
      return calendar;
    }

    async function init(){
      const tzSel = document.getElementById('tz');
      let calendar = makeCalendar(tzSel.value);
      calendar.render();

      // Detect event sources and load in priority: ICS > JSON > SAMPLE
      const { hasICS, hasJSON, base } = await detectSources();
      if(hasICS){
        calendar.addEventSource({
          url: base + 'events.ics',
          format: 'ics'
        });
      } else if(hasJSON){
        try {
          const res = await fetch(base + 'events.json', { cache: 'no-store' });
          const data = await res.json();
          calendar.addEventSource(data);
        } catch (e){
          console.warn('Failed to load events.json, using samples', e);
          calendar.addEventSource(SAMPLE_EVENTS);
        }
      } else {
        calendar.addEventSource(SAMPLE_EVENTS);
      }

      // View switchers
      document.querySelectorAll('[data-view]').forEach(btn => {
        btn.addEventListener('click', () => {
          calendar.changeView(btn.dataset.view);
        });
      });

      // Timezone switcher
      tzSel.addEventListener('change', () => {
        const currentDate = calendar.getDate();
        calendar.destroy();
        calendar = makeCalendar(tzSel.value);
        calendar.render();
        // Re-attach sources
        (async () => {
          const { hasICS, hasJSON, base } = await detectSources();
          if(hasICS){
            calendar.addEventSource({ url: base + 'events.ics', format: 'ics' });
          } else if(hasJSON){
            const res = await fetch(base + 'events.json', { cache: 'no-store' });
            const data = await res.json();
            calendar.addEventSource(data);
          } else {
            calendar.addEventSource(SAMPLE_EVENTS);
          }
          calendar.gotoDate(currentDate);
        })();
      });
    }

    init();
  </script>
</body>
</html>

