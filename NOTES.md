# HW2 notes

Answer each question in a few sentences. Be specific: name the function, the error or the command.

## What did you try?
I created the virtual environment and ran .venv\Scripts\activate in PowerShell to set up pytest, then implemented AlreadySignedUpError and UnknownEventError in errors.py, sign_up, cancel, and place in event.py, and add_event, event, handle, and attendance in club.py

## What broke, and how did you fix it?
Running .venv\Scripts\activate failed with a PSSecurityException / UnauthorizedAccess error because PowerShell script execution was disabled, which I fixed with Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser. Running python -m pytest also initially failed with NotImplementedError across unimplemented methods until I finished errors.py, event.py, and club.py

## What would you do differently next time?
I would check my PowerShell execution policy and activate .venv before running setup commands, and run python -m pytest after implementing each individual method rather than all at once.