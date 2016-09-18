#Django-account-starter
a collection of django account views

## Setup
add django_account_starter to project


in settings.py


to installed apps, add:

```
INSTALLED_APPS = (
    'django_account_starter',
)
```


to load login urls prior to hitting urls.py:

```
from django.core.urlresolvers import reverse_lazy

LOGIN_REDIRECT_URL = reverse_lazy('/')
LOGIN_URL = reverse_lazy('login')
LOGOUT_URL = reverse_lazy('logout')
```


to enable emailing of password,
complete the following settings:

```
EMAIL_HOST = ''
EMAIL_HOST_USER = ''
EMAIL_HOST_PASSWORD = ''
EMAIL_PORT =
EMAIL_USE_TLS =
```


in urls.py
```
    url(r'^account/', include('django_account_starter.urls')),
```

and I think you are done