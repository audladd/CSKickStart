eecs280.org
=============
EECS 280 course web site

The HTML content in `/docs/` is publicly available at [https://eecs280staff.github.io/eecs280.org/](https://eecs280staff.github.io/eecs280.org/).


## Contributing
To update the website, modify the files in `/docs/`, commit to `master` and push to GitHub.

Test locally by navigating to http://localhost:8000/
```shellsession
$ cd docs/
$ python3 -m http.server
```

Verify W3C HTML5 compatibility
```shellsession
$ cd docs/
$ html5validator --root .
```

## Calendar

The home page uses FullCalendar to render the official staff Google Calendar. It is configured to recolor events based on their title, and displays a popup with the event's title and location. To configure for future semesters:

- Update the Google Calendar ID.
  - Follow the guide on this page to retrieve the calendar ID: https://fullcalendar.io/docs/google-calendar
  - Modify the calendar ID that is passed to `calendar.renderCalendar` in `index.html`.
- Label all calendar events with the following patterns:
  - `Lecture*`: Displayed in color 'tomato'
  - `Office Hours*`: Displayed in color 'blueberry'
  - `Proffice Hours*`: Displayed in color 'basil'
  - (All other events are displayed in the default color light-blue.)
- If the Google Calendar API key is not working, follow the guide on this page to obtain a new API key: https://fullcalendar.io/docs/google-calendar
