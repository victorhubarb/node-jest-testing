# Jest/Node.js testing <a name="readme-top"></a>
![Static Badge](https://img.shields.io/badge/status-completed-green?style=for-the-badge)

## Table of Contents 
* [Title and Cover Image](#title-and-cover-image)
* [Badges](#badges)
* [Table of Contents](#table-of-contents)
* [Project Description](#project-description)
* [Features and Application Demonstration](#features-and-application-demonstration)
* [Project Access](#project-access)
* [Technologies Used](#technologies-used)

## Project Description
This project focuses on implementing comprehensive testing in Node.js applications. It covers various types of testing such as static, unit, and integration tests. The project utilizes tools like Jest for unit testing and SuperTest for integration testing, providing a robust framework for ensuring code reliability and quality.
Throughout the development of this project, a testing culture has been established, emphasizing the importance of code consistency and error prevention. Various testing techniques and best practices have been integrated, such as using ESLint for static code analysis, Jest for unit tests, and SuperTest for simulating HTTP requests in integration tests.
<p align="right">(<a href="#readme-top">back to top</a>)</p>
 
## Features
- **Static Testing**:
  - Implements static code analysis using ESLint to ensure code follows established conventions and best practices.
  - Detects issues like missing modules or poor code clarity without executing the code.

- **Unit Testing**:
  - Implements unit tests for validating the behavior of small, isolated parts of the application.
  - Uses Jest as the primary testing framework for writing and running unit tests.
  - Includes native assertion methods to compare values and analyze test results.

- **Integration Testing**:
  - Tests combined modules and their interactions using SuperTest to simulate HTTP requests.
  - Ensures different parts of the application work seamlessly together.

- **Test Coverage and Reporting**:
  - Uses Jest's `--coverage` flag to generate test coverage reports, helping identify untested code paths.
  - Highlights potential false positives even with high coverage percentages.

- **Advanced Jest Features**:
  - Utilizes `jest.spyOn()` to monitor method calls and enhance assertion capabilities.
  - Applies `jest.fn()` to mock functions and simulate specific behaviors during testing.
  - Runs asynchronous tests using `then` and `await` for handling promises.
  - Leverages `test.each()` to simplify repetitive test cases with dynamic inputs.

- **Test Skipping and Hooks**:
  - Incorporates the `skip` method to temporarily bypass specific tests during development.
  - Configures hooks (beforeAll, afterAll) to handle setup and teardown for test environments.
<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Project Access

### Prerequisites
- **Node.js**: Required for running the project. [Install Node.js here](https://nodejs.org/en/download/).
- **Jest**: The testing framework used in this project. Install it by following the official [Jest documentation](https://jestjs.io/docs/en/getting-started).
- **SuperTest**: Required for integration testing, which can be installed via npm.


### Getting the Code
You can obtain the source code of the project in two ways:
- **Download ZIP**:
  - [Download the ZIP file here](https://github.com/victorhubarb/node-jest-testing/archive/refs/heads/main.zip). After downloading, unzip it on your computer and open the project in your preferred IDE.
- **Clone via Git**:
  ```bash
  # Open your terminal (or command prompt)
  git clone https://github.com/victorhubarb/node-jest-testing.git
  
  # Navigate to the project directory
  cd node-jest-testing
<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Running the Project
Once you have the project setup, follow these steps to run the application:
- **Install Dependencies**:
  ```bash
  # Navigate to the project directory if you haven't already
  cd node-testing-course

  # Install the necessary packages
  npm install

- **Run the Tests**:
  ```bash
  # Run all tests
  npm test

  # Generate coverage report
  npm test -- --coverage
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
## Technologies Used

- **Node.js**: A JavaScript runtime built on Chrome's V8 JavaScript engine, used for building the backend of the application.
- **Jest**: A JavaScript testing framework used for running unit tests and generating test coverage reports.
- **SuperTest**: A module used to test HTTP assertions, particularly useful for testing integration with Node.js servers.
- **ESLint**: A static code analysis tool for identifying problematic patterns found in JavaScript code.
- **Express.js**: A minimal and flexible Node.js web application framework used for handling routes and server logic.
<p align="right">(<a href="#readme-top">back to top</a>)</p>
