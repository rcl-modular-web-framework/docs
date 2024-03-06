---
title: Module Micro Frontend
description: A module can provide micro front end pages and components for integration into a web application
has_children: false
nav_order: 4
parent: Module
---

# Micro Frontend

A micro frontend is a reusable page or component provided in a module that can be integrated in a web application.

## Creating Micro Frontend

A micro frontend should be created with a ``Razor Class Library`` with views and pages. The project is included in the module's solution using the naming convention {project-name}.UI, eg. ``RCL.MWF.Subscription.UI``.

## Pages 

Pages are may be include in a folder named ``Pages``. Pages can also be organized in ``Areas`` using the recommended convention for Areas.

## Components

``View Components`` must be used to create components. The components should be created in a folder named ``View Components``, the Views should be created in a folder named ``Views``.

## Listing Entry Pages

The entry page(s) of the micro front end must be listed in the README.md page of the module. A suggested navigation structure for the pages should be provided.

## Environment Variables

Environment variables must be provided to micro front end using the ``Options`` pattern. The classes used to store the variables must be listed in the module's README.md. The classes must be stored in a folder named ``Options``.

## NuGet Packages

The micro frontend must be made available via a NuGet package. NuGet packages can be publicly hosted on NuGet or privately in on-premise servers or private cloud.

The name and version of the NuGet package must be specified in the module's README.md file.

