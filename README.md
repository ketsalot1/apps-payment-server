This is an experimental integration with PayPal's Digital Goods payment
service.

Using Python 2.6+ and a [virtualenv](http://pypi.python.org/pypi/virtualenv),
install like this:

    pip install -r requirements.txt

To get things set up, run:

    python paymentserver/manage.py syncdb
    python paymentserver/manage.py runserver 0.0.0.0:8380

To make the paypal redirects work you must currently run everything from:

    http://localhost:8380/

To override settings copy the local settings file:

    cp paymentserver/settings_local-dist.py paymentserver/settings_local.py

And start up the server with that file:

    python paymentserver/manage.py runserver --settings=paymentserver.settings_local 0.0.0.0:8380
