---
title: Module Data
description: A module must manage its own data
has_children: false
nav_order: 2
parent: Module
---

# Data Management

A module must manage its own data. Data can be persisted in cloud storage such as an Azure SQL Database.

A project should be created in the module's solution to define the entities of the database. The project should be named following the convention: {project}.DataContext, eg. ``RCL.MWF.Subscription.DataContext``.

## Database Entities

Database entities should be created in a folder named ``Models`` in the data context project. 

In the README.md file for the module's solution, each database entity used by module must be listed.

## Database Context

The data context should be defined in a folder named ``Context``. It is recommended that ``Entity Framework`` be used to manage data.

## Database Creation and Migrations

The solution must contain two projects to handle database creation and migration. One for the production and the other for the development environment. The name of the projects should follow the convention : {project-name}.DataMigrations.{environment} , eg. ``RCL.MWF.DataMigrations.Production``.

In the README.md file for the module instruction must be provided on how to run the code first database creation and migrations. It should also specify the cloud database that should be used and the IDE for data migrations.

A user will need to download the Data projects data migrations in their Visual Studio IDE connected to a cloud database.

## NuGet Packages

The database entities and data context can be made public via a NuGet package. NuGet packages can be publicly hosted on NuGet or privately in on-premise servers or private cloud.

The name and version of the NuGet package must be specified in the module's README.md file.