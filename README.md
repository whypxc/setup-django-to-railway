<h1>How to deploy Django to Railway.app</h1>
<br>

<h2>Pip Install</h2>
<br>
<h3>Gunicorn</h3> <code>pip install gunicorn</code>
<h3>Whitenoise</h3> <code>pip install whitenoise</code>
<br>

<h2>Requirements</h2>
<br>
<h3>Create requirements.txt file.</h3>
<h3>In cmd write</h3><code>freeze > requirements.txt</code>
<br>

<h2>Settings</h2>
<br>
<code>import os
<br>
ALLOWED_HOSTS = ["name app"]
<br>
INSTALLED_APPS = ['whitenoise.runserver_nostatic',]
<br>
MIDDLEWARE = ["whitenoise.middleware.WhiteNoiseMiddleware",]
<br>
STATIC_URL = '/static/'
STATIC_ROOT = os.path.join(BASE_DIR, 'static')
STATICFILES_STORAGE="whitenoise.storage.CompressedManifestStaticFilesStorage"</code>
