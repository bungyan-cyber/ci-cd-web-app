# CI/CD with GitHub Actions

This project sets up a CI/CD pipeline for a simple Flask web application using GitHub Actions.

## Requirements

- GitHub account
- Heroku account
- Python

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone git@github.com:yourusername/ci-cd-web-app.git
   cd ci-cd-web-app
   ```

2. **Run the Application Locally**:
   ```bash
   cd app
   pip install -r requirements.txt
   python app.py
   ```

3. **Run the Tests**:
   ```bash
   pytest tests
   ```

## CI/CD Pipeline

The GitHub Actions pipeline is configured to:
- Run tests using pytest
- Lint the code using flake8
- Deploy the application to Heroku

## Deploy to Heroku

1. Create a Heroku app:
   ```bash
   heroku create your-heroku-app-name
   ```

2. Set the Heroku API key in GitHub Secrets:
   - Go to your repository on GitHub.
   - Click on Settings > Secrets > New repository secret.
   - Add `HEROKU_API_KEY` with your Heroku API key.

3. Push your code to GitHub:
   ```bash
   git add .
   git commit -m "Initial commit: Set up CI/CD pipeline"
   git push origin main
   ```

## Access the Deployed Application

After deployment, you can access the application at `https://your-heroku-app-name.herokuapp.com`.

## License

This project is licensed under the MIT License.
