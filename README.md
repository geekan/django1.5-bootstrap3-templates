django1.5-bootstrap3-templates
==============================

Here are all you should modify. Only a little files.

settings.py:
=======
```
INSTALLED_APPS += (
    'django_bootstrap_example',
    'registration',
    'crispy_forms',
)

ACCOUNT_ACTIVATION_DAYS=7
EMAIL_HOST='localhost'
EMAIL_PORT=8025
```

urls.py
=======
```
urlpatterns += patterns('',
    url(r'^$', TemplateView.as_view(template_name='base.html'), name='index' ),
    url(r'^accounts/', include('registration.backends.default.urls')),
)
```

templates
=====
Just copy the `registration` folder and `base.html`.

Test Email Auth
=====
`python -m smtpd -n -c DebuggingServer localhost:8025`

Tasks
=====
* [Partly] registration and login
