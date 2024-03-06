---
title: Module Service
description: A module must provide public services for other  modules to communicate with it
has_children: false
nav_order: 3
parent: Module
---

# Module Service

Modules will communicates with other modules through public services. A service is provided through and Interface and Extension so that it can be injected through dependency injection.

Services are created in a class library project with the following naming convention  {project-name}.Core, eg. ``RCL.MWF.Subscription.Core``

Services and their interfaces should be stored in a folder named ``Services`` in the project.

## Listing Services

The public services provided by the module must be listed on the README.md file in the module's solution.

## Service Environment Variables

Environment variables must be provided to services using the ``Options`` pattern in ASP.NET. The classes used to store the variables must be listed in the module's README.md.

## Exposing the Services

Services are exposed publicly using extensions and through ``Dependency Injection``. The extension must be created a folder named ``Extensions``.

## Injecting Services

Services are injected in the ``Program.cs`` of a web application or function app. Other methods can also be used to inject the services in applications or for testing.

Example code must be provided on how to inject the service in an application.

## NuGet Packages

The service can be made public via a NuGet package. NuGet packages can be publicly hosted on NuGet or privately in on-premise servers or private cloud.

The name and version of the NuGet package must be specified in the module's README.md file.