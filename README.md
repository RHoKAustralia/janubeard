== README

Janubeard is simple web application which allows a user to take photos of themselves
with a beard overlayed on the photo.  Afterwards the user can share the photo with
their friends via facebook or twitter.

=== Getting started:

==== Cloudinary:
This project uses cloudinary to store images and You will need to add it's secret
keys in a `.env` file in your project root:
```
export CLOUDINARY_KEY=[your cloudinary api key]
export CLOUDINARY_NAME=[your cloudinary name]
export CLOUDINARY_SECRET=[your cloudinary secret]
```

==== Postgres:
This project uses postgresql to store data about the photos taken.  You will need
to be running Postrgres locally to develop against this app.

On OSX with postgres installed via homebrew this command will work: `postgres -D /usr/local/var/postgres`

To setup your database you will want to do the following
- `rake db:create`
- `rake db:migrate`


=== Deploying:

In order to deploy you will want to get the rights to deploy to `janubeard.herokuapp.com`.
Link heroku to your local repo:  `heroku git:remote janubeard`
And whenever you want to deploy: `git push heroku master`
