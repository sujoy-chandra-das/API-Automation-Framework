# API Automation Testing Framework

## Overview
`api-automation-testing-framework` is a comprehensive framework designed for automating API testing. It utilizes `pytest` for writing and running tests, with integrated logging and configuration management.

## Features
- **Automated Testing**: Easily create and run automated tests for your APIs.
- **Logging**: Integrated logging to capture detailed test run information.
- **Configuration Management**: Centralized configuration management for easy setup and maintenance.
- **Extensible**: Easily extend and customize for different API testing needs.

## Getting Started

### Prerequisites
- Python 3.x
- `pytest`
- `requests`
- `pytest-html` (for HTML reports)
- `pytest-cov` (for coverage reports)

Install the required packages:
```bash
pip install -r requirements.txt

Running Tests
Run all tests and generate an HTML report and coverage report:
        pytest



### Directory Structure:

       api-automation-framework/
├── .github/
│   └── workflows/
│       └── regression_suite.yml
├── .venv/
├── data/
│   └── test_data.json
├── Logs/
│   └── test_log.txt
├── reports/
│   ├── report_2025-05-02_13-33-44.html
│   └── report_2025-05-02_19-35-02.html
├── tests/
│   ├── reports/
│   └── test_users_api.py
├── utils/
│   └── api_client.py
├── venv/
├── conftest.py
├── pytest.ini
├── README.md
└── requirements.txt

Regression_suite.yml
👉 GitHub Actions workflow file for running CI/CD. It defines steps like installing dependencies, running tests, generating reports, and uploading logs.

test_data.json
👉 Stores test input data used in your test scripts, such as mock user information, API payloads, or configurations.src/: Source files including API client and configuration parser.
tests/: Test cases and fixtures.

test_log.txt
👉 Captures console output or log details after test execution (especially from pytest > logs/test_log.txt). Useful for debugging and historical tracking.

report_*.html
👉 Automatically generated HTML reports from pytest --html plugin. These are test result summaries for visual review.

test_users_api.py
👉 Main test file with your actual test functions, e.g., API test validations using pytest.

api_client.py
👉 Helper functions for sending API requests, managing sessions, or wrapping requests logic. Promotes code reuse and clean test files.


### Contributing
Contributions are welcome! Please submit a pull request or create an issue for any changes or suggestions.

License
This project is licensed under the MIT License.
