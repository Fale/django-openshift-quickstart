# Django-Openshift quickstart

## OpenShift
To run this on openshift you need to (only the first time):

    rhc env set OPENSHIFT_PYTHON_WSGI_APPLICATION=openshift/wsgi.py --app [APP_NAME]

and then, as usual, push to your openshift repo:

    git push

## Local server
To run this on your local machine to devel, just run:

    python3 manage.py runserver
