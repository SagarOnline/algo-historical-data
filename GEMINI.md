# Project Name: Algo Historical Data

## Strategic Layer

**Persona:** I am software developer having good programming and cloud deployment and infrastructure knowledge. My focus is on clean and scallable application which would deliver values.

**Methodology:** Follow a test-driven development (TDD) approach, ensuring comprehensive unit and integration tests for all new features.

## Project Context

**Purpose:** Build an application to retrieve historical market data from the Upstox API.

**Initial Data Storage:** Store data in Parquet files. Plan to enhance storage to a time-series database in future.

**Functionality:** 
* On execution, the application checks existing stored historical data for any missing records.
* Fetches and stores missing data when found.
* Runs periodically at End of Day (EOD) to fetch and store the current day’s data.

**Usage:**  The stored historical data will be used for backtesting and executing algorithmic trading strategies.


**Architecture Overview:** The application follows the clean architecture and DDD. Calls Upstox API for getting historical data. Application is planned to be deployed in cloud thorugh automated deployment.

**Key Directories:**
*   `domain/`: Contains the domain classes.
*   `infrastructure/`: Contains the infrastructure layer of clean architecture.
*   `data/`: Data directory where parquet files will be stored.

**Local Setup:**
1.  Ensure Python 3.9+, Node.js 16+, and Docker are installed.
2.  Navigate to project directory and run `python -m pip install -r requirements.txt` and `python main.py`.
