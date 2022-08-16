## WhiteNoise

WhiteNoise takes care of best-practices for you, for instance:

- Serving compressed content (gzip and Brotli formats, handling Accept-Encoding and Vary headers correctly).

- Setting far-future cache headers on content which won’t change.

### Installation

Install with:

    pip install whitenoise

### QuickStart for Django apps

Edit your settings.py file and add WhiteNoise to the MIDDLEWARE list, above all other middleware apart from Django’s
SecurityMiddleware:

    MIDDLEWARE = [
        # ...
        "django.middleware.security.SecurityMiddleware",
        "whitenoise.middleware.WhiteNoiseMiddleware",
        # ...
    ]

Want forever-cacheable files and compression support? Just add this to your settings.py:

    STATICFILES_STORAGE = "whitenoise.storage.CompressedManifestStaticFilesStorage"

### QuickStart for other WSGI apps

To enable WhiteNoise you need to wrap your existing WSGI application in a WhiteNoise instance and tell it where to find
your static files. For example:

    from whitenoise import WhiteNoise
    
    from my_project import MyWSGIApp
    
    application = MyWSGIApp()
    application = WhiteNoise(application, root="/path/to/static/files")
    application.add_files("/path/to/more/static/files", prefix="more-files/")

