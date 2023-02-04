<h1>How to setup Django to Railway.app</h1>

<h2>Pip Install</h2>
<h3>Gunicorn</h3> <pre>pip install gunicorn</pre>
<h3>Whitenoise</h3> <pre>pip install whitenoise</pre>
<br>

<h2>Requirements</h2>
<h3>Create requirements.txt file.</h3>
<h3>In cmd write</h3>
<pre>pip freeze > requirements.txt</pre>
<h3>In requirements.txt delete "+6.g3b105b4" line 25</h3>
<br>

<h2>Settings:</h2>
<pre class="notranslate">
import os

INSTALLED_APPS = ['whitenoise.runserver_nostatic',]

MIDDLEWARE = ["whitenoise.middleware.WhiteNoiseMiddleware",]

STATIC_URL = '/static/'
STATIC_ROOT = os.path.join(BASE_DIR, 'static')
STATICFILES_STORAGE="whitenoise.storage.CompressedManifestStaticFilesStorage"
</pre>

