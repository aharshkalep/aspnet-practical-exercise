# To-do List Application

## Development Tasks

Development tasks are tasks with a technical description of what needs to be done. Choose the task track that matches your chosen architecture:

### Option 1: Monolithic MVC Architecture (Recommended for Regular Students)

* T01-M: Basic project setup and Entity Framework configuration.
    * Create the *TodoListApp.WebApp* ASP.NET Core MVC project and add it to the solution file.
    * Enable built-in .NET code analysis tools; add the StyleCop NuGet package as a dependency.
    * Add the required Entity Framework Core NuGet packages: `Microsoft.EntityFrameworkCore.SqlServer`, `Microsoft.EntityFrameworkCore.Tools`, and `Microsoft.EntityFrameworkCore.Design`.
    * Create a `TodoListDbContext` class in the *TodoListApp.WebApp* project and configure the database connection string in the application config file.
    * Configure `TodoListDbContext` as a dependency in the dependency injection container.
    * Create and apply the initial database migration using EF Core tools.
    * Add initial data seed for all entities (at least 3 records per table).
* T02-M: Implement Epic 1 functionality in the *TodoListApp.WebApp* application.
* T03-M: Implement Epic 2 functionality in the *TodoListApp.WebApp* application.
* T04-M: Implement Epic 3 functionality in the *TodoListApp.WebApp* application.
* T05-M: Implement Epic 4 functionality in the *TodoListApp.WebApp* application.
* T06-M: Implement Epic 5 functionality in the *TodoListApp.WebApp* application.
* T07-M: Implement Epic 6 functionality in the *TodoListApp.WebApp* application.
* T08-M: Implement Epic 7 functionality in the *TodoListApp.WebApp* application.
* T09-M: Implement Epic 8 frontend functionality in the *TodoListApp.WebApp* application.
* T10-M: Design and implement good-looking browser UI.

### Option 2: 3-Tier Architecture with Separate Web API (Advanced Students Only)

* T01-A: Basic project setup and Entity Framework configuration.
    * Create all C# projects (*TodoListApp.WebApp*, *TodoListApp.WebApi*, and any shared class libraries) and add them to the solution file; configure project dependencies.
    * Enable built-in .NET code analysis tools in C# projects; add the StyleCop NuGet package as a dependency to all C# projects.
    * Add the required Entity Framework Core NuGet packages to the *TodoListApp.WebApi* project: `Microsoft.EntityFrameworkCore.SqlServer`, `Microsoft.EntityFrameworkCore.Tools`, and `Microsoft.EntityFrameworkCore.Design`.
    * Create a `TodoListDbContext` class in the *TodoListApp.WebApi* project and configure the database connection string in the application config file.
    * Configure `TodoListDbContext` as a dependency in the *TodoListApp.WebApi* app's dependency injection container.
    * Create and apply the initial database migration using EF Core tools.
    * Add initial data seed for all entities (at least 3 records per table).
* T02-A: Implement Epic 1 [backend](https://en.wikipedia.org/wiki/Frontend_and_backend) functionality in the *TodoListApp.WebApi* application.
    * Add a new service interface named `ITodoListDatabaseService` and a data class named `TodoList` to the *TodoListApp.WebApi* project.
    * Add a new service class named `TodoListDatabaseService` to the *TodoListApp.WebApi* project to manage to-do lists in the database; configure the service as a dependency in the *TodoListApp.WebApi* app.
    * Add a new controller class named `TodoListController` to the *TodoListApp.WebApi* project; resolve service dependencies using constructor injection.
    * US01: Add new methods to the `TodoListDatabaseService` to get the list of to-do lists from the database; make all necessary changes in other classes and methods.
    * US01: Add a new model class named `TodoListModel` to the *TodoListApp.WebApi* project.
    * US01: Implement the REST endpoint in the *TodoListApp.WebApi* project to get the list of to-do lists; the list must be in JSON format. Use the `TodoListModel` class as the model in the controller methods.
    * US02: Add new methods to the `TodoListDatabaseService` to add a new to-do list; make all necessary changes in other classes and methods.
    * US02: Implement the REST endpoint in the *TodoListApp.WebApi* project to add a new to-do list; the input data must be in JSON format; and the endpoint must return meaningful status codes in case of errors.
    * US03: Add new methods to the `TodoListDatabaseService` to delete an existing to-do list; make all necessary changes in other classes and methods.
    * US03: Implement the REST endpoint in the *TodoListApp.WebApi* project to delete an existing to-do list; the endpoint must return meaningful status codes in case of errors.
    * US04: Add new methods to the `TodoListDatabaseService` to update an existing to-do list's data; make all necessary changes in other classes and methods.
    * US04: Implement the REST endpoint in the *TodoListApp.WebApi* project to update an existing to-do list's data; the endpoint must return meaningful status codes in case of errors.
* T03-A: Implement Epic 1 frontend functionality in the *TodoListApp.WebApp* application.
    * Add a new service interface named `ITodoListWebApiService` and a data class named `TodoList` to the *TodoListApp.WebApp* project.
    * Add a new service class named `TodoListWebApiService` to the *TodoListApp.WebApp* project to manage to-do lists in the web API app using REST API; configure the service as a dependency in the *TodoListApp.WebApp* app.
    * Add a new controller class named `TodoListController` to the *TodoList.WebApp* project; resolve service dependencies using constructor injection.
    * US01: Add a new class named `TodoListWebApiModel` to the TodoListApp.WebApp project.
    * US01: Add a new method to the `TodoListWebApiService` to get the list of to-do lists using the REST API. Use the `TodoListWebApiModel` class as the model for REST API endpoints.
    * US01: Add a new view to the *TodoList.WebApp* project and a new method to the `TodoListController` class to show the list of to-do lists to the user using the browser UI.
    * US02: Add a new method to the `TodoListWebApiService` to add a new to-do list using the REST API.
    * US02: Add a new view to the *TodoList.WebApp* project and a new method to the `TodoListController` class to allow a user to add a new to-do list using the browser UI.
    * US03: Add a new method to the `TodoListWebApiService` to delete an existing to-do list using the REST API.
    * US03: Add a new view to the *TodoList.WebApp* project and a new method to the `TodoListController` class to allow a user to delete an existing to-do list using the browser UI.
    * US04: Add a new method to the `TodoListWebApiService` to update an existing to-do list's data using the REST API.
    * US04: Add a new view to the *TodoList.WebApp* project and a new method to the `TodoListController` class to allow a user to update an existing to-do list's data using the browser UI.
* T04-A: Implement Epic 2 backend functionality in the *TodoListApp.WebApi* application.
* T05-A: Implement Epic 2 frontend functionality in the *TodoListApp.WebApp* application.
* T06-A: Implement Epic 3 backend functionality in the *TodoListApp.WebApi* application.
* T07-A: Implement Epic 3 frontend functionality in the *TodoListApp.WebApp* application.
* T08-A: Implement Epic 4 backend functionality in the *TodoListApp.WebApi* application.
* T09-A: Implement Epic 4 frontend functionality in the *TodoListApp.WebApp* application.
* T10-A: Implement Epic 5 backend functionality in the *TodoListApp.WebApi* application.
* T11-A: Implement Epic 5 frontend functionality in the *TodoListApp.WebApp* application.
* T12-A: Implement Epic 6 backend functionality in the *TodoListApp.WebApi* application.
* T13-A: Implement Epic 6 frontend functionality in the *TodoListApp.WebApp* application.
* T14-A: Implement Epic 7 functionality in the *TodoListApp.WebApp* application.
* T15-A: Implement Epic 8 frontend functionality in the *TodoListApp.WebApp* application.
* T16-A: Design and implement good-looking browser UI.


## Delivery Plan

The delivery plan contains a list of technical tasks distributed across 5 phases. Choose the plan that matches your chosen architecture:

### Option 1: Monolithic MVC Architecture (Recommended for Regular Students)

| Task | Phase 0 | Phase 1 | Phase 2 | Phase 3 | Phase 4 |
|------|---------|---------|---------|---------|---------|
| T01-M| +       |         |         |         |         |
| T02-M|         | +       |         |         |         |
| T03-M|         |         | +       |         |         |
| T04-M|         |         | +       |         |         |
| T05-M|         |         |         | +       |         |
| T06-M|         |         |         | +       |         |
| T07-M|         |         |         |         | +       |
| T08-M|         |         |         |         | +       |
| T09-M|         |         |         |         | +       |
| T10-M|         |         |         |         | +       |

### Option 2: 3-Tier Architecture with Separate Web API (Advanced Students Only)

| Task | Phase 0 | Phase 1 | Phase 2 | Phase 3 | Phase 4 |
|------|---------|---------|---------|---------|---------|
| T01-A| +       |         |         |         |         |
| T02-A|         | +       |         |         |         |
| T03-A|         | +       |         |         |         |
| T04-A|         |         | +       |         |         |
| T05-A|         |         | +       |         |         |
| T06-A|         |         | +       |         |         |
| T07-A|         |         | +       |         |         |
| T08-A|         |         |         | +       |         |
| T09-A|         |         |         | +       |         |
| T10-A|         |         |         | +       |         |
| T11-A|         |         |         | +       |         |
| T12-A|         |         |         |         | +       |
| T13-A|         |         |         |         | +       |
| T14-A|         |         |         |         | +       |
| T15-A|         |         |         |         | +       |
| T16-A|         |         |         |         | +       |


## Phase Checklists

Use phase checklists to track your development progress. Choose the checklist that matches your chosen architecture:

### Option 1: Monolithic MVC Architecture

#### Phase 0: Project Setup & Entity Framework

- [ ] T01-M: ASP.NET Core MVC project is created and added to the solution file.
- [ ] T01-M: Built-in .NET code analysis tools are enabled; StyleCop NuGet package is added as a dependency and configured properly.
- [ ] T01-M: Required Entity Framework Core NuGet packages are added to the project.
- [ ] T01-M: `TodoListDbContext` is created, configured in the application config file, and registered in the dependency injection container.
- [ ] T01-M: Initial database migration is created and applied successfully.
- [ ] T01-M: Initial data seed is added for all entities (at least 3 records per table).
- [ ] All changes are committed and pushed to the remote repository.
- [ ] The solution builds without errors.

#### Phase 1: Basic Infrastructure & EP01

- [ ] T02-M: Implement [Epic 1 (EP01): To-Do Lists](user-stories.md#epic-1-ep01-to-do-lists) functionality in the *TodoListApp.WebApp* application.
- [ ] All changes are committed and pushed to the remote repository.
- [ ] There are no major or critical issues or blockers found during building the solution.

#### Phase 2: EP02 and EP03

- [ ] T03-M: Implement [Epic 2 (EP02): Tasks](user-stories.md#epic-2-ep02-tasks) functionality in the *TodoListApp.WebApp* application.
- [ ] T04-M: Implement [Epic 3 (EP03): Assigned Tasks](user-stories.md#epic-3-ep03-assigned-tasks) functionality in the *TodoListApp.WebApp* application.
- [ ] All changes are committed and pushed to the remote repository.
- [ ] There are no major or critical issues or blockers found during building the solution.

#### Phase 3: EP04 and EP05

- [ ] T05-M: Implement [Epic 4 (EP04): Search](user-stories.md#epic-4-ep04-search) functionality in the *TodoListApp.WebApp* application.
- [ ] T06-M: Implement [Epic 5 (EP05): Tagging Tasks](user-stories.md#epic-5-ep04-tagging-tasks) functionality in the *TodoListApp.WebApp* application.
- [ ] All changes are committed and pushed to the remote repository.
- [ ] There are no major or critical issues or blockers found during building the solution.

#### Phase 4: EP06-EP08

- [ ] T07-M: Implement [Epic 6 (EP06): Commenting Tasks](user-stories.md#epic-6-ep05-commenting-tasks) functionality in the *TodoListApp.WebApp* application.
- [ ] T08-M: Implement [Epic 7 (EP07): Users](user-stories.md#epic-7-ep06-users) functionality in the *TodoListApp.WebApp* application.
- [ ] T09-M: Implement [Epic 8 (EP08): Menu](user-stories.md#epic-8-ep08-menu) functionality in the *TodoListApp.WebApp* application.
- [ ] T10-M: Design and implement good-looking browser UI.
- [ ] All changes are committed and pushed to the remote repository.
- [ ] There are no major or critical issues or blockers found during building the solution.

### Option 2: 3-Tier Architecture with Separate Web API

#### Phase 0: Project Setup & Entity Framework

- [ ] T01-A: All C# projects are created and added to the solution file; project dependencies are configured.
- [ ] T01-A: Built-in .NET code analysis tools are enabled in C# projects; StyleCop NuGet package is added as a dependency to all C# projects and configured properly.
- [ ] T01-A: Required Entity Framework Core NuGet packages are added to the *TodoListApp.WebApi* project.
- [ ] T01-A: `TodoListDbContext` is created in the *TodoListApp.WebApi* project, configured in the application config file, and registered in the dependency injection container.
- [ ] T01-A: Initial database migration is created and applied successfully.
- [ ] T01-A: Initial data seed is added for all entities (at least 3 records per table).
- [ ] All changes are committed and pushed to the remote repository.
- [ ] The solution builds without errors.

#### Phase 1: Basic Infrastructure & EP01

- [ ] T02-A: Implement [Epic 1 (EP01): To-Do Lists](user-stories.md#epic-1-ep01-to-do-lists) backend functionality in the *TodoListApp.WebApi* application.
- [ ] T03-A: Implement [Epic 1 (EP01): To-Do Lists](user-stories.md#epic-1-ep01-to-do-lists) frontend functionality in the *TodoListApp.WebApp* application.
- [ ] All changes are committed and pushed to the remote repository.
- [ ] There are no major or critical issues or blockers found during building the solution.

#### Phase 2: EP02 and EP03

- [ ] T04-A: Implement [Epic 2 (EP02): Tasks](user-stories.md#epic-2-ep02-tasks) backend functionality in the *TodoListApp.WebApi* application.
- [ ] T05-A: Implement [Epic 2 (EP02): Tasks](user-stories.md#epic-2-ep02-tasks) frontend functionality in the *TodoListApp.WebApp* application.
- [ ] T06-A: Implement [Epic 3 (EP03): Assigned Tasks](user-stories.md#epic-3-ep03-assigned-tasks) backend functionality in the *TodoListApp.WebApi* application.
- [ ] T07-A: Implement [Epic 3 (EP03): Assigned Tasks](user-stories.md#epic-3-ep03-assigned-tasks) frontend functionality in the *TodoListApp.WebApp* application.
- [ ] All changes are committed and pushed to the remote repository.
- [ ] There are no major or critical issues or blockers found during building the solution.

#### Phase 3: EP04 and EP05

- [ ] T08-A: Implement [Epic 4 (EP04): Search](user-stories.md#epic-4-ep04-search) backend functionality in the *TodoListApp.WebApi* application.
- [ ] T09-A: Implement [Epic 4 (EP04): Search](user-stories.md#epic-4-ep04-search) frontend functionality in the *TodoListApp.WebApp* application.
- [ ] T10-A: Implement [Epic 5 (EP05): Tagging Tasks](user-stories.md#epic-5-ep04-tagging-tasks) backend functionality in the *TodoListApp.WebApi* application.
- [ ] T11-A: Implement [Epic 5 (EP05): Tagging Tasks](user-stories.md#epic-5-ep04-tagging-tasks) frontend functionality in the *TodoListApp.WebApp* application.
- [ ] All changes are committed and pushed to the remote repository.
- [ ] There are no major or critical issues or blockers found during building the solution.

#### Phase 4: EP06-EP08

- [ ] T12-A: Implement [Epic 6 (EP06): Commenting Tasks](user-stories.md#epic-6-ep05-commenting-tasks) backend functionality in the *TodoListApp.WebApi* application.
- [ ] T13-A: Implement [Epic 6 (EP06): Commenting Tasks](user-stories.md#epic-6-ep05-commenting-tasks) frontend functionality in the *TodoListApp.WebApp* application.
- [ ] T14-A: Implement [Epic 7 (EP07): Users](user-stories.md#epic-7-ep06-users) functionality in the *TodoListApp.WebApp* application.
- [ ] T15-A: Implement [Epic 8 (EP08): Menu](user-stories.md#epic-8-ep08-menu) frontend functionality in the *TodoListApp.WebApp* application.
- [ ] T16-A: Design and implement good-looking browser UI.
- [ ] All changes are committed and pushed to the remote repository.
- [ ] There are no major or critical issues or blockers found during building the solution.
