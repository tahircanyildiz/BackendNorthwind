# <p align="center"> .Net backend Project </p>

## Contents
- [Getting Started](#getting-started)
  * [Installation](#installation)
  * [Usage](#usage)
- [Tech Stack](#tech-stack)

## Getting Started

### Installation

1. Clone the repo:

   ```sh
   git clone https://github.com/tahircanyildiz/BackendNorthwind.git
   ```
2. Open the `NortwindBackend.sln` file with `Visual Studio`
3. Open the `appsettings.json` file in the `WebApi` folder and enter your own database connection string
4. Open `Package Manager Console - Default Project: DataAccess` and run the following commands for migrate database:

   ```sh
   update-database
   ```
   `NOTE:`
   ```sh
    Or Migrates automatically when you start the project
   ```
   
5. Right click on the `WebAPI` project (layer) from the `Solution Explorer` and select `Set as Startup Project` 
6. Start the project with `WebApi` in Visual Studio. Web API is ready and running!

### Usage
 
After running the Web API, you can make HTTP requests like:
   
   ```sh
   https://localhost:23963/api/`CONTROLLER_NAME`/`METHOD_NAME`
   ```
 
   `CONTROLLER_NAME` => Each .cs file located in the `WebAPI.Controllers` folder (For example CONTROLLER_NAME for `ProductsController`: Products )
   <br><br>
   `METHOD_NAME` => All of the methods in each .cs file in the `WebAPI.Controllers` folder
 
#### Sample HTTP GET requests:

1. List all Products:
   ```sh
   https://localhost:23963/api/Products/getall
   ```
2. List a brand by categoryId:
   ```sh
   https://localhost:23963/api/Products/getbycategory?categoryId=3
   ```
3. List all Categories :
   ```sh
   https://localhost:23963/api/Categories/getall
   ```

## Tech Stack
| Technology / Library | Version |
| ------------- | ------------- |
| .NET | 5,.0 |
| Autofac | 6.4.0 |
| Autofac.Extensions.DependencyInjection | 8.0.0 |
| Autofac.Extras.DynamicProxy | 6.0.1 |
| FluentValidation | 11.1.0 |
| Microsoft.AspNetCore.Authentication.JwtBearer | 6.0.7 |
| Microsoft.AspNetCore.Http | 2.2.2 |
| Microsoft.AspNetCore.Http.Abstractions | 2.2.0 |
| Microsoft.AspNetCore.Features | 5.0.17 |
| Microsoft.EntityFrameworkCore | 6.0.7 |
| Microsoft.EntityFrameworkCore.Tools | 6.0.7 |
| Microsoft.EntityFrameworkCore.Design | 6.0.7 |
| Microsoft.EntityFrameworkCore.InMemory | 6.0.7 |
| Microsoft.EntityFrameworkCore.SqlServer | 6.0.7 |
| Microsoft.Extensions.Configuration | 6.0.1 |
| Microsoft.Extensions.Configuration.Json | 6.0.1 |
| Microsoft.Extensions.Configuration.Binder | 6.0.0 |
| Microsoft.Extensions.DependencyInjection.Json | 6.0.0 |
| Microsoft.IdentityModel.Tokens | 6.12.2 |
| System.IdentityModel.Tokens.Jwt | 6.12.2 |
| Swashbuckle.AspNetCore | 6.2.3 |






