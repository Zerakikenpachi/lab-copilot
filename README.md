# Library App

## Description

Library App is a sample .NET 8.0 solution for managing a library system. It demonstrates clean architecture principles, separation of concerns, and test-driven development. The application supports patron management, book loans, membership renewals, and data persistence using JSON files. It includes a console interface for user interaction and a suite of unit tests.

## Project Structure

- AccelerateDevGitHubCopilot.sln
- README.md
- src/
  - Library.ApplicationCore/
    - Library.ApplicationCore.csproj
    - Entities/
    - Enums/
    - Interfaces/
    - Services/
  - Library.Console/
    - Library.Console.csproj
    - Program.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - CommonActions.cs
    - appSettings.json
    - Json/
      - Authors.json
      - Books.json
      - BookItems.json
      - Loans.json
      - Patrons.json
  - Library.Infrastructure/
    - Library.Infrastructure.csproj
    - Data/
- tests/
  - UnitTests/
    - UnitTests.csproj
    - PatronFactory.cs
    - LoanFactory.cs
    - ApplicationCore/
      - LoanService/
        - ExtendLoan.cs
        - ReturnLoan.cs

## Key Classes and Interfaces

- **Entities**
  - `Author`, `Book`, `BookItem`, `Patron`, `Loan`  
    Core domain models representing library data.

- **Enums**
  - `MembershipRenewalStatus`, `LoanReturnStatus`, `LoanExtensionStatus`  
    Status codes for operations.

- **Interfaces**
  - `IPatronRepository`, `ILoanRepository`  
    Abstractions for data access.
  - `IPatronService`, `ILoanService`  
    Abstractions for business logic.

- **Services**
  - `PatronService`, `LoanService`  
    Implement business logic for patrons and loans.

- **Infrastructure**
  - `JsonData`  
    Loads and saves data from JSON files.
  - `JsonPatronRepository`, `JsonLoanRepository`  
    Implement repository interfaces using JSON persistence.

- **Console Application**
  - `ConsoleApp`  
    Main user interface logic for searching patrons, viewing loans, and managing memberships.

## Usage

1. **Build the Solution**
   ```sh
   dotnet build
   ```
2. **Run the Application**
   ```sh
   dotnet run --project src/Library.Console/Library.Console.csproj
   ```
3. **Run Unit Tests**
   ```sh
   dotnet test
   ```

## Features

- **Patron Management**
  - Add, remove, and update patron information.
  - View patron details and loan history.

- **Book Management**
  - Add, remove, and update book information.
  - View book details and availability.

- **Loan Management**
  - Create, extend, and return book loans.
  - View loan details and status.

- **Membership Renewal**
  - Renew patron memberships.
  - View renewal status and history.

- **Data Persistence**
  - All data is persisted in JSON files for simplicity and ease of use.

## Technologies Used

- **.NET 8.0**
  - The application is built using the latest .NET 8.0 SDK.

- **C# 11.0**
  - The application uses C# 11.0 features and syntax.

- **JSON**
  - Data is persisted in JSON format for simplicity and ease of use.

- **Entity Framework Core (InMemory)**
  - Used for data access and manipulation in the application.

- **xUnit**
  - The unit tests are written using the xUnit testing framework.

- **FluentAssertions**
  - Used for fluent and expressive assertions in unit tests.

## Getting Started

To get started with the Library App, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/library-app.git
   ```
2. Navigate to the project directory:
   ```sh
   cd library-app
   ```
3. Build the solution:
   ```sh
   dotnet build
   ```
4. Run the application:
   ```sh
   dotnet run --project src/Library.Console/Library.Console.csproj
   ```
5. Enjoy managing your library!

## Contributing

Contributions are welcome! If you have suggestions or improvements, feel free to submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the need for a simple and effective library management system.
- Built with passion and dedication to clean architecture and best practices.
