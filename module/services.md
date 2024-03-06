---
title: Module Service
description: A module must provide public services for other  modules to communicate with it
has_children: false
nav_order: 3
parent: Module
---

# Module Service

Modules will communicates with other modules and to the web application through public services. A service is provided through and Interface and Extension so that it can be used through dependency injection.

Services are created in a class library project with the following naming convention  {project-name}.Core, eg. ``RCL.MWF.Subscription.Core``

Services and the interfaces should be stored in a folder named ``Services`` in the project.

## Listing Services

The services provided by the module must be listed on the README.md file in the module's solution.

## Service Environment Variables

Environment variables must be provided to services using the ``Options`` pattern. The classes used to store the variables must be listed in the module's README.md. The classes must be stored in a folder named ``Options``.

## Exposing the Services

Services are exposed publicly using extensions and through ``Dependency Injection``. The extension must be created a folder named ``Extensions``.

## Injecting Services

Services are injected in the ``Program.cs`` of a web application. Other methods can also be used to inject the services in other types of applications or for testing.

Example code must be provided on how to inject the service.

## Helper Classes

The service may provide helper classes. These classes are usually static classes and must be stored in a folder named ``Helpers``. A list of helpers classes must be provided in the README.md file of the module.

## NuGet Packages

The service must be made available via a NuGet package. NuGet packages can be publicly hosted on NuGet or privately in on-premise servers or private cloud.

The name and version of the NuGet package must be specified in the module's README.md file.