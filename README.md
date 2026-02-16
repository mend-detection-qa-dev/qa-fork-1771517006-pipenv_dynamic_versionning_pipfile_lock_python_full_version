# Pipenv Test Case 6: Pipfile.lock with python_full_version

## What This Tests
Tests detection of Python version from Pipfile.lock when Pipfile has no requires section, using `python_full_version` field.

## Expected
3.11.4 found through PipfileLockPythonFullVersion

## Files
- `Pipfile` - No requires section
- `Pipfile.lock` - Contains `"python_full_version": "3.11.4"` in _meta.requires

## Expected Behavior
Your version detection tool should detect **Python 3.11.4** from Pipfile.lock.

## Priority
This is the **fourth priority** detection method for Pipenv projects. When both `python_version` and `python_full_version` are present in the lock, `python_full_version` takes precedence.

## Note
Pipfile.lock provides exact version specifications and is preferred when Pipfile doesn't have a requires section.
