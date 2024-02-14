# BadgeMaker C# .NET 8

Badge Maker is a command-line application written in C# that generates employee badges from randomly generated employee data retrieved from the Random User Generator API.

## Installation

To run Badge Maker on your local maching, follow these steps:

1. Clone this repository to your local maching using Git:

- `git clone https://github.com/RandyYanish/BadgeMaker.git`

2. Navigate to the project directory:

- `cd BadgeMaker`

3. Build the project using the .NET CLI:

- `dotnet build`

4. Run the application:

- `dotnet run`

## Usage

By default, Badge Maker retrieves employee data from the Random User Generator API. However, you can also provide your own employee data in CSV format. Here's how:

1. Prepare your CSV file with the following columns: FirstName, LastName, ID, PhotoUrl. You can use Excel or any other spreadsheet software to create the CSV file.

2. Save the CSV file in the `data` directory of the project.

3. Modify the `GetEmployees()` method in the `Program.cs` file to read data from your CSV file instead of the API:

```csharp
List<Employee> employees = Util.ReadCSV("path/to/your/csv/file.csv");
```

4. Build and run the application again:

```
dotnet build
dotnet run
```

Badge Maker will now generate employee badges using the data from your CSV file.

### Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

### Licence

This project is licensed under the MIT License. See the [LICENSE](../LICENSE) file for details
