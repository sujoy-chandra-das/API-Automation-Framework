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

🔧 Core Components
.github/workflows/regression_suite.yml
➤ Implemented CI/CD using GitHub Actions. The pipeline installs dependencies, runs automated tests, saves logs (logs/test_log.txt), and generates HTML test reports for every push and pull request to main.

test_data.json
➤ Maintains mock input data for test coverage such as API payloads and expected values. Centralizing this data enables parameterized testing and easier data updates.

Logs/test_log.txt
➤ Captures execution logs during pytest runs. Configured the pipeline and local execution to redirect console outputs here for better traceability and post-run analysis.

reports/report_*.html
➤ Integrated pytest-html to auto-generate timestamped test reports. These provide a clean UI for reviewing pass/fail status, captured logs, and metadata.

 
🧪 Testing Layer
tests/test_users_api.py
➤ Developed test cases for user-related APIs using Pytest. Validated status codes, response payloads, and headers. All tests follow assert-based validations with fixtures from conftest.py.

conftest.py
➤ Created reusable fixtures for setup/teardown processes, base URL management, and data injection to keep test files DRY and maintainable.

🛠️ Utility Layer
utils/api_client.py
➤ Built a custom API client module to handle GET, POST, PUT, and DELETE requests. Wrapped request logic for headers, tokens, and payloads to reduce duplication and improve readability in test scripts.

### Contributing
Contributions are welcome! Please submit a pull request or create an issue for any changes or suggestions.

License
This project is licensed under the MIT License.
