# Jira-Github-Integration

This project demonstrates a DevOps workflow that integrates GitHub Issues with Jira using a lightweight Flask API hosted on an AWS EC2 instance. The Flask app runs on port 5000, receiving POST requests from a GitHub Webhook whenever a new issue is created in the repository. The webhook sends a JSON payload that the Flask API parses to detect the /jira command inside the issue body. When found, the API communicates with the Jira REST API using an API token to automatically create a Jira ticket with the relevant details. This approach eliminates manual ticket creation, keeps development and project management tools in sync, and provides a foundation for further automation. The design is simple, lightweight, and easy to extend for additional triggers or bi-directional integrations.

Python 3 & Flask – For building the lightweight API to process GitHub webhook events and communicate with Jira.

GitHub Webhooks – To trigger POST requests with JSON payloads when issues are created.

Jira REST API – For programmatically creating Jira tickets using API tokens.

AWS EC2 (Ubuntu) – Hosting the Flask app and exposing it on port 5000 for webhook access.

Requests Library (Python) – To handle HTTP POST/GET requests between Flask and Jira APIs.

Git & GitHub – For version control, repository management, and collaboration.



