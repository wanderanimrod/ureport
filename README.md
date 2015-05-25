U-report  
=========

This is the U-report dashboard built on data collected by RapidPro.

Built for UNICEF by Nyaruka - http://nyaruka.com

Getting Started
================

Install dependencies
```
% virtualenv env
% source env/bin/activate
% pip install -r pip-requires.txt
```

Link up a settings file (you'll need to create the postgres db first, username: 'ureport' password: 'nyaruka')
```
% ln -s ureport/settings.py.postgres ureport/settings.py
```

Sync the database, add all our models and create our superuser
```
% python manage.py syncdb
% python manage.py migrate
% python manage.py createsuper
```

Ensure you have lessc on your path. If you don't you can install it with [npm](https://www.npmjs.com/)
```
npm install -g less
```

At this point everything should be good to go, you can start with:

```
% python manage.py runserver
```

Note that the endpoint called for API calls is by default 'localhost:8001', you can uncomment the RAPIDPRO_API line in settings.py.postgres to go against production servers.