## ASP.NET 6 Core application made with C#, Entity Framework Core, and SQL Server.

## PROJECT DEPENDENCIES
- [Visual Studio (IDE)](https://visualstudio.microsoft.com/).
- [SQL Server 2022 Developer](https://www.microsoft.com/en-us/sql-server/sql-server-downloads).
- [SQL Server Management Studio](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16&redirectedfrom=MSDN).

Include this in the Visual Studio installation:
- ASP.NET and web development.
- Azure development.
- .NET desktop development.

## PROJECT SETUP
- When creating a project, select: ASP.NET Core Web App (Model-View-Controller) template.
- Select .NET 6 framework.

## DB SETUP
- While in Visual Studio, navigate to the dependencies folder and right click
- In Manage NuGet packages, search and install Microsoft.EntityFrameworkCore.SqlServer.
- Also install Microsoft.EntityFrameworkCore.Tools.
- Create a 'Data' folder inside the main directory.
- Create a class file inside that folder and name it in this format:" YourProjectDbContext ".
- This class inherits from the DbContext class from Microsoft.EntityFrameworkCore.
- Inside the Models directory, create a Domain folder.
- Inside the Domain folder, create a class, named based on your DB table.
- Populate the class with your column names.
- Navigate to the main program: 'Program.cs'.
- Add the code:" builder.Services.AddDbContext<YourProjectDbContext>(options => options.UseSqlServer(builder.Configuration("YourProjectConnectionString"))) ",
which are imported from the Data folder and the Microsoft.EntityFrameworkCore.
- Go to 'appsettings.json' and create a connection string property below the AllowedHosts.
- Code:" "ConnectionStrings":{ "YourProjectConnectionString": "server=YourServerName;database=YourDBName;Trusted_connection=true" } ".
- In the navigation bar, go to Tools -> NuGet Package Manager -> Package Manager Console.
- Run the command:" Add-Migration "Initial Migration" " and then press enter.
- Run another command:" Update-Database " and press enter.
- Refresh your Databases folder in the Microsoft SQL Server Management Studio.

## AND YOU ARE SET!
- Make sure you are importing (using) the packages/class files you are implementing in your code.


## =================================================
ASP.NET Core
============

[![.NET Foundation](https://img.shields.io/badge/.NET%20Foundation-blueviolet.svg)](https://www.dotnetfoundation.org/)
[![MIT License](https://img.shields.io/github/license/dotnet/aspnetcore?color=%230b0&style=flat-square)](https://github.com/dotnet/aspnetcore/blob/main/LICENSE.txt) [![Help Wanted](https://img.shields.io/github/issues/dotnet/aspnetcore/help%20wanted?color=%232EA043&label=help%20wanted&style=flat-square)](https://github.com/dotnet/aspnetcore/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22) [![Good First Issues](https://img.shields.io/github/issues/dotnet/aspnetcore/good%20first%20issue?color=%23512BD4&label=good%20first%20issue&style=flat-square)](https://github.com/dotnet/aspnetcore/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)
[![Discord](https://img.shields.io/discord/732297728826277939?style=flat-square&label=Discord&logo=discord&logoColor=white&color=7289DA)](https://aka.ms/dotnet-discord)

ASP.NET Core is an open-source and cross-platform framework for building modern cloud-based internet-connected applications, such as web apps, IoT apps, and mobile backends. ASP.NET Core apps run on [.NET](https://dot.net), a free, cross-platform, and open-source application runtime. It was architected to provide an optimized development framework for apps that are deployed to the cloud or run on-premises. It consists of modular components with minimal overhead, so you retain flexibility while constructing your solutions. You can develop and run your ASP.NET Core apps cross-platform on Windows, Mac, and Linux. [Learn more about ASP.NET Core](https://learn.microsoft.com/aspnet/core/).

## Get started

Follow the [Getting Started](https://learn.microsoft.com/aspnet/core/getting-started) instructions.

Also check out the [.NET Homepage](https://www.microsoft.com/net) for released versions of .NET, getting started guides, and learning resources.

See the [Triage Process](https://github.com/dotnet/aspnetcore/blob/main/docs/TriageProcess.md) document for more information on how we handle incoming issues.

## How to engage, contribute, and give feedback

Some of the best ways to contribute are to try things out, file issues, join in design conversations,
and make pull-requests.

* [Download our latest daily builds](./docs/DailyBuilds.md)
* Follow along with the development of ASP.NET Core:
    * [Community Standup](https://live.asp.net): The community standup is held every week and streamed live on YouTube. You can view past standups in the linked playlist.
    * [Roadmap](https://aka.ms/aspnet/roadmap): The schedule and milestone themes for ASP.NET Core.
* [Build ASP.NET Core source code](./docs/BuildFromSource.md)
* Check out the [contributing](CONTRIBUTING.md) page to see the best places to log issues and start discussions.

## Reporting security issues and bugs

Security issues and bugs should be reported privately, via email, to the Microsoft Security Response Center (MSRC)  secure@microsoft.com. You should receive a response within 24 hours. If for some reason you do not, please follow up via email to ensure we received your original message. Further information, including the MSRC PGP key, can be found in the [Security TechCenter](https://technet.microsoft.com/en-us/security/ff852094.aspx).

## Related projects

These are some other repos for related projects:

* [Documentation](https://github.com/aspnet/Docs) - documentation sources for https://learn.microsoft.com/aspnet/core/
* [Entity Framework Core](https://github.com/dotnet/efcore) - data access technology
* [Runtime](https://github.com/dotnet/runtime) - cross-platform runtime for cloud, mobile, desktop, and IoT apps
* [Razor](https://github.com/dotnet/razor) - the Razor compiler and tooling for working with Razor syntax (.cshtml, .razor)

## Code of conduct

See [CODE-OF-CONDUCT](./CODE-OF-CONDUCT.md)
