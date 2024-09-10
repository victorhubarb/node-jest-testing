# Bookstore API Testing <a name="readme-top"></a>
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
This project focuses on implementing various testing strategies for a REST API that manages a bookstore system. The API includes functionality for managing books, authors, and publishers. This project leverages testing frameworks and tools such as Jest and SuperTest to ensure the reliability and maintainability of the API, using static analysis, unit testing, and integration testing.
<p align="right">(<a href="#readme-top">back to top</a>)</p>
 
## Features
- **Static Testing**:
  - ESLint is used for static code analysis to ensure code follows best practices and proper formatting without executing the code.
  
- **Unit Testing**:
  - Jest is employed to create unit tests, focusing on the behavior of small, isolated parts of the bookstore API.
  - Native assertion methods are used for comparing values and testing expected outputs.

- **Integration Testing**:
  - Integration tests are run using SuperTest, simulating HTTP requests to ensure the proper interaction between different parts of the API.

- **Test Coverage**:
  - Jest’s `--coverage` flag is used to generate test coverage reports, helping identify untested portions of the API.
<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Project Access

### Prerequisites
- **Node.js**: You need Node.js installed to run this project. [Download Node.js here](https://nodejs.org/en/download/).
- **Jest**: This project uses Jest for testing. You can install it by following the [Jest documentation](https://jestjs.io/docs/en/getting-started).
- **SuperTest**: Required for running integration tests.

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
After downloading the project, follow these steps to set it up and run the tests:
- **Install Dependencies**:
  ```bash
  npm install

- **Run the Tests**:
  ```bash
  npm test

- **Generate coverage report**:
  ```bash
  npm test -- --coverage
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
## Technologies Used
- **Node.js**: JavaScript runtime for building the server-side API.
- **Express**: Web framework for Node.js used for handling API routes and logic.
- **Jest**: JavaScript testing framework used for unit tests and coverage reports.
- **SuperTest**: Tool for testing HTTP assertions, used in integration testing.
- **Knex.js**: SQL query builder used to interact with the SQLite database.
- **SQLite3**: Database engine used for storing the bookstore data.
- **ESLint**: Static code analysis tool to ensure code quality.
<p align="right">(<a href="#readme-top">back to top</a>)</p>
