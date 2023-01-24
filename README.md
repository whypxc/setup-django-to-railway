How to deploy Django to Railway.app
<br>

Library
<br>
1. Gunicorn - 'pip install gunicorn'
2. Whitenoise - 'pip install whitenoise'
<br>

Requirements
<br>
Create requirements.txt file.
In cmd write 'freeze > requirements.txt'
<br>

Settings
<br>
1. 'import os'
2. 'ALLOWED_HOSTS = ["name app"]'
3. 'INSTALLED_APPS = ['whitenoise.runserver_nostatic',]'
4. 'MIDDLEWARE = ["whitenoise.middleware.WhiteNoiseMiddleware",]'
5.  'STATIC_URL = '/static/'
    STATIC_ROOT = os.path.join(BASE_DIR, 'static')
    STATICFILES_STORAGE="whitenoise.storage.CompressedManifestStaticFilesStorage"'


