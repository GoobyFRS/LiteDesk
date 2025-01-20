# GoobyDesk

Peppermint.sh no longer appears to be maintained and was left in an unusable state. I would contribute but I have no desire to learn Typescript as a Network Engineer. Thus GoobyDesk. It is barebones and simple. No Databases. I don't like them. User Accounts and Tickets databases are json files for simplicity.

**Current Version:** Major.Minor.Patch - 0.1.2

## How GoobyDesk works

- GoobyDesk is a python3.12 Flask project that by default runs at ```http://127.0.0.1:5000```.
- Landing page is a basic Service Desk form.
- User provided _email_ and _subject_ are used to create an auto-email.
- The script will monitor the configured inbox every 2 minutes for replies.
- User replies are appended to the "notes" in tickets.json

## Linux Project Setup

```shell
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python3 ./app.py
```

CTRL+C to break. ```deactivate``` to clean up.

## Windows Project Setup

```shell
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

CTRL+C to break. ```deactivate``` to clean up.

### Goals and Roadmap

- Implement ability to close tickets from the dashboard.
- OAuth2.0 Support for Email Authentication.
- Fine tune email reply handling.
- HTML Form validation.
- File locking and retry support.
- Mutli-user support
