# Quote of the Day

A small Flask application that displays a random programming quote and provides
the quote as JSON through an API endpoint.

## Run Locally

1. Create and activate a virtual environment:

	```bash
	python -m venv .venv
	```

	Windows PowerShell:

	```powershell
	.\.venv\Scripts\Activate.ps1
	```

2. Install the dependencies:

	```bash
	pip install -r requirements.txt
	```

3. Start the application:

	```bash
	python app.py
	```

4. Open http://localhost:5000 in a browser.

## Deploy

1. Push the project files to a Git repository.
2. Create a new Python web service with your hosting provider and connect the
	repository.
3. Use the following deployment settings:

	- **Build command:** `pip install -r requirements.txt`
	- **Start command:** `gunicorn app:app`
	- **Python version:** Use the provider's supported Python 3 version.

4. Deploy the service and open the public URL provided by the host.

The start command uses `app:app`, which means the host loads the `app` Flask
object from `app.py`.

## Endpoints

- `/` displays a randomly selected quote in HTML.
- `/api/quote` returns a randomly selected quote as JSON.

Example API response:

```json
{
  "quote": "Talk is cheap. Show me the code. — Linus Torvalds"
}
```
## Render Static Website URL

This website can also be visited [here.](https://lab-6-quote-app.onrender.com)