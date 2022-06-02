# trackertracker

An app to keep track of tracking numbers. Built with Django and Postgres, with front-end views built with Jinja templating and Tailwind CSS via the `django-tailwind` plugin.

## App Structure

### Main Page

There's a main view of the app that will display each package being tracked, which include an optional title, a tracking number, the corresponding service, and a progress bar denoting the current status of the package.

Packages in the main view are sorted by ship date, most recent first.

Pagination is a big ol' TODO.

### Signup and Login

Standard Django signup and login flows are used. I may update this to use token-based authentication if I build a mobile app based on this app. 

### Adding Tracking Numbers

There are four ways that tracking numbers can be ingested into the app.

1. Manually inputting the tracking number on the front-end. (Duh.)
2. Forwarding emails that contain tracking numbers to a specific email on the server.
3. Parsing through a Gmail inbox to look for emails that contain tracking numbers. (TODO)
4. Third-party integrations with various services (Amazon, Shopify, etc.) to look for tracking numbers. (TODO)

### Additional Backend Stuff

* notifications
* cron- or queue-based re-checking of tracking statuses

## Hosting and Deployment

Extreme TBD.