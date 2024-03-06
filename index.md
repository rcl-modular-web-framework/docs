---
title: Introduction
description: Introducing the RCL Modular Web Framework
has_children: false
nav_order: 1
---

# Introduction

The RCL Modular Web Framework (MWF) sets out an architectural pattern to compose a web application from modules. The MWF is applied to the .NET Framework and ASP.NET Core.

This document outlines the specification for the MWF.

## Module

A module is a solution comprised of a set of defined projects that includes data, services and micro front ends. Modules can communicate with other modules using the services that they expose publicly.

Modules are created following the broad concepts of the Domain Driven Design pattern. Modules are designed within a given context, eg. Identity or Payments. Each module must be reusable in many varied web applications.

## Web Application

A web application will comprise of one or more modules. Modules are integrated into a web application as NuGet Packages.  

