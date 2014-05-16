Django
======

People to follow
================
@gyvanrossum
@jezdez
@doughellmann
@ericholscher
@agodwin

#django on freenode

 - Python web framework

Strengths
---------
  - Developer friendly
  - Included suite of apps
  - DRY friendly features
  - Build a whole lot for not very little

Weaknesses
----------
  - Monolithic (Battieries included)
  - Change things means that there are in django may not work

Django is Python 3 compatable (Still not a strong adoption)


Installing Django
-----------------

    virtualenv ./django
    . ./bin/activate
    pip install virtualenvwrapper
    pip install django

    When django is installed it puts django_admin.py on your path.

Django projects are like the settings and configurations and the applications
are going to be the different modules you import into django.

Internet > Webserver > WSGI > URLs > View > Templates & Forms & Models

The first place that the WSGI object will hit is the URLs. Django will find the
matching url view and pass the request object to the view.o

A View is a python method that accepts a request and returns an http response.
Convention is `views.py`. Views should be small
`django.shortcuts.render` is used to return an http response. Render finds the
template and oasses in a context to return the client.

Templates are rendered uring avaliable context.
Context is something that you will pass back into the template

Views should be very skinny and models should be very fat.

`django.contrib.*` is where you will find all the applications that are builtin
to django.

Models - Think SqlAlchemy but for django
Model Methods - Used for modifying an instance of the data.
`from django.core.urlresolvers import reverse` - Finds url for name of view

Managers - convention `managers.py`
Managers can be used to extend modelso

Migrations - Used are used for migrating schema data.
South managed migrations for django. You should setup an initial migration
before using south. Otherwise you will need to fake it so that south can play
catchup.
`pip install south`
Uses the django `manage.py`
`manage.py schemamigration blog --auto`

Fabric - Another must have tool
Python module that will execute code in a remote or local shell. Think Grunt for
Python.

vim: ft=markdown tw=80 sts=2 colorcolumn=80
