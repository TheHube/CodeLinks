# Feature: Web Application Scraping and Monitoring

## 1. User Stories to be negotiated

### Scenario: Specify URL for Scraping
    Given the user is on the web application configuration page
    When the user specifies a URL to scrape
    Then the web application should remember the specified URL

### Scenario: Scraping and Storing Metrics
    Given the web application is running
    When 90 seconds pass
    Then the web application should scrape the specified URL
    And store the metrics in the database using Entity Framework Core

### Scenario: View Stored Metrics
    Given the user is on the web application metrics page
    When the user views the stored metrics
    Then the web application should display the server's memory usage over time

### Scenario: Receive Alert for High Memory Usage
    Given the web application is running
    When the server's memory usage exceeds 10,000 bytes
    Then the web application should alert the user

### Scenario: Continuous Automatic Operation
    Given the web application is configured
    When the application is running
    Then it should automatically perform scraping and metric storage every 90 seconds

### Scenario: User-Friendly Interface
    Given the user is on the web application interface
    When the user interacts with the configuration, metrics, and alert sections
    Then the web application should provide a clean and user-friendly experience

### Scenario: Database Connection Management
    Given the user is on the web application database configuration page
    When the user sets up and manages the database connection details
    Then the web application should use the specified database for storing metrics

### Scenario: Discord Bot Connection
    Given the Discord bot is configured
    When the bot connects to the same database as the web application
    Then it should retrieve and post alerts in the designated channel

### Scenario: Post Discord Alert
    Given the server's memory usage exceeds 10,000 bytes
    When the Discord bot posts an alert in the designated channel
    Then the user should receive timely notification

### Scenario: Include Relevant Information in Discord Alert
    Given the Discord bot posts an alert
    When the alert is displayed
    Then it should include timestamp, current memory usage, and additional details for better understanding
