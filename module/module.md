---
title: Module
description: A web application is comprised of one or more modules
has_children: true
nav_order: 2
---

# Module

A module is created following the Domain Driven Design pattern. A module is bounded within a defined context, eg. Identity or Payments. A module is a solution that comprise various projects with responsibility for :

 - Managing data
 - Providing services and functions
 - Providing micro frontend pages

 ## General Requirements

 A module must be developed as a Visual Studio Solution that contains various projects as defined in this specification. The solution must contain a README.md file. The README.md file should contain the name of the module in the format of an assembly name , eg. ``RCL.MWF.Subscription``. It should also contain a brief description of what is the purpose of the module.

 A module must be hosted in GitHub where users can download and customize the module if necessary. 

 ## Data Management

 A module will comprise of a project that defines the data entities and context for the management of the modules data. The project is a class library and should follow the naming syntax : {project-name}.DataContext, eg. ``RCL.MWF.Subscription.DataContext`` . An additional project should be created to handle Database creation and migration with a cloud database, eg. Azure SQL. Ideally there should be two projects to handle development and production scenarios.

Example solution for a module, illustrating the data management projects:

```
RCL.MWF.Subscription (.sln)
|
----> RCL.MWF.Subscription.DataContext (.csproj)
|
----> RCL.MWF.Subscription.DataMigrations.Production (.csproj)
|
----> RCL.MWF.Subscription.DataMigrations.Development (.csproj)
```

If the module does not manage data, this section can be omitted.

## Services

A module should provide a way to communicate with other modules. This is accomplished with services that exposed publicly. The services are created in a project following this naming convention : {project-name}


