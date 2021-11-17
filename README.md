# Introduction




# Setup

Create virual environment and install dependencies for local development:

```
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

The application requires the following environment variables specific the databricks workspace and security token that you're using for testing, development and deployment. Substitute your own values between the angled brackets:

```
N/A
```

Exporting variables doesn't make for a great development experience so I recommend using the enviroment manager tools of your editor and for testing create a ./pytest.ini that looks like this:

```
[pytest]
env =
    
```

**REMINDER: do NOT commit any files that contain security tokens**


# Example


# Build

Build python wheel:
```
python setup.py sdist bdist_wheel
```

There is a CI build configured for this repo that builds on main origin on a private Azure DevOps service. It doesn't yet push to PyPi.

# Test

Dependencies for testing:
```
pip install --editable .
```

Run tests:
```
pytest
```

Test Coverage:
```
pytest --cov=mycelium --cov-report=html
```

View the report in a browser:
```
./htmlcov/index.html
```


