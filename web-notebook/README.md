## Web Notebook

### Idea

The common activity I use for myself is keeping data records, which I can track and aggregate later. There is no particular activity I want to track, it's more about having an ability to add a simple handler that will create a new page on the site, where I can save new items.

One problem I need to solve is how to authenticate to the site. One option is to create an admin role that can generate link for registration, then I can send it to a new person on the site. The first user I can create manually in the database.

To use the notebook I need to create a framework that will need only an update in the configuration file to create a new structure of tabs on the site. I may use one style or choose style for each user or tab from predefined ones.

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
```

All tables in the database should generated automatically

### Configuration

Environment variables:

- `PORT` - the port where API will listen
- `HTML_TEMPLATES` - the folder with static HTML templates

### Notes
