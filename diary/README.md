## Diary

### Idea

The common activity I use for myself is keeping data records, which I can track and aggregate later. There is no particular activity I want to track, it's more about having an ability to track different activities day by day.

Example configuration for it:

```yaml
- name: sleeping hours
  fields:
    - name: hours
      type: integer
      title: How many hours I slept today
    - name: feeling_good
      type: integer
      title: How am I feeling well (from 1 to 10)?
  notifications:
    - at: "12:00"
      message: "add record to diary about your previous day"
      type: "notify-send"
```

Since there is a need to send notifications, the app should have two parts:

- interface to fill the data
- commands to show data with pretty view
- crontab generator with notifications

Example usage:

```bash
$ diary add today "sleeping hours"
> How many hours I slept today?
8
> How am I feeling well (from 1 to 10)?
7
Thanks! Have a Good Day!
$ diary edit today "sleeping hours"
$ diary show today "sleeping hours"
$ diary show last 10 "sleeping hours"
$ diary show first 10 "sleeping hours"
$ diary update notifications "sleeping hours"
```

### Configuration

Environment variables:

- `DB_DSN` - connection string for database (SQLite or PostgreSQL)

### Notes

All tables in the database should generated automatically
