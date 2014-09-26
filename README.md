# Django-Openshift quickstart

## Development
If you would like to develop something ontop of this you will only have to:

* Add the application folder in the root
* Mention the application in the `INSTALLED_APPS` array in the `openshift/settings.py` file

You are now ready to deploy.

The folders `static` and `templates` can be used to create the website layout parting it from your application for truly reusable applications.

## How to install
### OpenShift
To run this on openshift you need to (only the first time):

    rhc env set OPENSHIFT_PYTHON_WSGI_APPLICATION=openshift/wsgi.py --app [APP_NAME]

### Local server
The first time you want to run this on your local machine to devel, you have to run:

    python3 manage.py syncdb

This will create the sqlite database that is needed by the application.

## How to run
### OpenShift
As usual, push to your openshift repo:

    git push

### Local server
To run this on your local machine to devel, just run:

    python3 manage.py runserver
