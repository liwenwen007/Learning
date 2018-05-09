# Google_translation_API with Python

Please check the details in the reference. I will only highlight some tricky steps.

[Reference](https://cloud.google.com/translate/docs/quickstart): tutorial on making a Google Cloud Translation API request with curl.
It's very simple start.

## Get a private key (credentials)

Set up a GCP Console project to get the kay.
Notice: a billing account is needed. 

## python samples

Clone this [repo](https://github.com/GoogleCloudPlatform/python-docs-samples/tree/master/translate/cloud-client) and follow its instruction

You may encounter the following problem when you try _quickstart.py_
```
google.auth.exceptions.DefaultCredentialsError: Could not automatically determine credentials. Please set GOOGLE_APPLICATION_CREDENTIALS or
explicitly create credential and re-run the application.
```

Add two lines in _quickstart.py_
```Python
import os
os.environ["GOOGLE_APPLICATION_CREDENTIALS"]="key_path"
```

If there is Chinese in the codes, remember to add:
```Python
# -*- coding: UTF-8 -*-
```
