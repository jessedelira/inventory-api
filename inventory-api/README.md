<div>
  <h3>
    <b>
      Inventory API
    </b>
  </h3>
  <b>
    Open-source Inventory API
  </b>
  <p>
  </p>
</div>

Inventory API is an open-source project that is a RESTful API that allows users to manage their inventory. This project
is built with .NET Core & MySQL.

### Reason behind the project

Familiarize myself with .NET Core and MySQL.

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any
contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also
simply open an issue with the tag "enhancement".
Don't forget to give the project a star!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these steps.

### Prerequisites

This is a list things you need to use the Gym Tracker.

- [.NET Core](https://dotnet.microsoft.com/download)
    - Current Version targeted: .NET 8.0
- [Docker](https://docker.com)

### Installation

1. Clone the repo
    ```sh
    $ git clone https://github.com/jessedelira/inventory-api.git
    ```
2. Create MySQL container (Run in root of project)
    ```sh
    $ docker-compose up -d
    ```
3. Using your database management tool, create a database called `defaultdb` on the MySQL server
    - The connection string is already set up in the appsettings.json file

4. Create appsettings.json at root of project and add the following:
    ```json
    {
      "Logging": {
      "LogLevel": {
        "Default": "Information",
        "Microsoft.AspNetCore": "Warning"
      }
      },
      "AllowedHosts": "*",
      "ConnectionStrings": {
        "DefaultConnection": "server=localhost;port=3306;database=defaultdb;user=root;password=password"
      }
   }

   ```

5. Run the migrations
    ```sh
    $ dotnet ef database update
    ```
6. Finally, run `$ dotnet run inventory-api/inventory-api.csproj` to start the server or use Visual Studio/Rider to run the
   project.
