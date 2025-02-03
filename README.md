# HNG Internship Stage 1 - Number Classification API

This repository contains a Python Flask API that classifies numbers, providing interesting mathematical properties and a fun fact. This project was completed as part of the HNG Internship Stage 1 for the DevOps track.

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the API Locally](#running-the-api-locally)
- [API Usage](#api-usage)
  - [Endpoint](#endpoint)
  - [Request Parameters](#request-parameters)
  - [Response Format](#response-format)
    - [Successful Response (200 OK)](#successful-response-200-ok)
    - [Error Response (400 Bad Request)](#error-response-400-bad-request)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Description

This API takes an integer as input and returns various properties, including:
*   Whether the number is prime or not
*   Whether the number is a perfect number
*  Armstrong status
*   A list of number properties (armstrong, odd, even)
*   The sum of its digits
*   A fun fact about the number.

The API utilizes external resources to get the fun fact by calling [Numbers API](http://numbersapi.com/#42).

## Features

-   Accepts GET requests with a `number` parameter.
-   Returns responses in JSON format.
-   Provides appropriate HTTP status codes (200 for success, 400 for bad request, 500 for server error).
-   Includes a fun fact about the given number using Numbers API.
-   Handles CORS to be accessible from different origins.

## Technology Stack

-   Python 3.6+
-   Flask (for web framework)
-   requests (for fetching fun facts from the Numbers API)
-   Flask_CORS (for enabling CORS)

## Getting Started

### Prerequisites

-   Python 3.6+
-   pip (Python package installer)

### Installation

1.  Clone the repository:
    ```bash
    git clone <your-github-repo-url>
    cd <repository-directory>
    ```
2.  Create and activate a virtual environment:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
3.  Install the dependencies:
    ```bash
    pip3 install -r requirements.txt
    ```

### Running the API Locally

To run the API locally:

```bash
python3 app.py
Use code with caution.
Markdown
The API will be available at http://127.0.0.1:5000/

API Usage
Endpoint
GET /api/classify-number

Request Parameters
number (required): An integer value for the API to classify.

Response Format
Successful Response (200 OK)
{
    "number": 371,
    "is_prime": false,
    "is_perfect": false,
    "properties": ["armstrong", "odd"],
    "digit_sum": 11,
    "fun_fact": "371 is an Armstrong number because 3^3 + 7^3 + 1^3 = 371"
}
Use code with caution.
JSON
Error Response (400 Bad Request)
{
    "number": "alphabet",
    "error": true,
    "message": "Invalid input"
}
Use code with caution.
JSON
Deployment
This application can be deployed using the following platforms:

Heroku

Render

AWS Elastic Beanstalk

Google Cloud App Engine

Railway

To deploy you should ensure that a requirements.txt includes all the needed dependencies. This file can be created by using the following command while the virtual environment is active:
pip freeze > requirements.txt

Contributing
Feel free to fork the repository and contribute to make it better.

License
This project is open source and available under the MIT license

**How to Use:**

1.  **Copy:** Copy the markdown text above.
2.  **Create File:** Create a new file named `README.md` in the root directory of your repository.
3.  **Paste:** Paste the copied content into the file.
4.  **Edit:** Replace `<your-github-repo-url>` with the actual URL of your GitHub repository.
5.  **Commit:** Commit and push the `README.md` file to your repository.

This will make your repository more professional and easy for other developers to use. Let me know if you have any other questions!
