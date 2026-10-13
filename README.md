# Lab 5 – Postman and APIs

Flask REST API that adds, reads, updates and deletes users in a SQLite database, tested with Postman.

## Run

```bash
python3 -m venv venv && source venv/bin/activate
pip install -r requirements.txt
python app.py
```

The app creates `database.db` on first run and listens on `http://localhost:5001`
(port 5000 is taken by AirPlay Receiver on macOS).

## Endpoints

| # | Endpoint | Method | Description |
|---|----------|--------|-------------|
| 1 | `/api/users` | GET | Get the list of all users in the database |
| 2 | `/api/users/<user_id>` | GET | Get a single user record that matches the id |
| 3 | `/api/users/add` | POST | Create a new user record |
| 4 | `/api/users/update` | PUT | Update a user record |
| 5 | `/api/users/delete/<user_id>` | DELETE | Delete a user record |

## Postman

`postman/` contains the **Flask user app** collection (one request per endpoint, each with a saved example)
and the **Flask user app - local** environment, which defines `base_url`. All requests use `{{base_url}}`.
Import both files in Postman and select the environment.
