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
        bash run_tests.sh



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

configurations/: Configuration files.
logs/: Log files generated during test runs.
src/: Source files including API client and configuration parser.
tests/: Test cases and fixtures.


### Contributing
Contributions are welcome! Please submit a pull request or create an issue for any changes or suggestions.

License
This project is licensed under the MIT License.


### `run_tests.sh` Example
```bash
#!/bin/bash

# Create reports directory if it doesn't exist
mkdir -p reports

# Run tests with HTML and coverage report
pytest --html=reports/test_report.html --cov=src --cov-report=html:reports/coverage_report
