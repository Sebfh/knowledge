# Howto: Start a ASP.NET MVC4 Project

This document holds a summary of command and tricks I use when working on [ASP.NET MVC4](http://www.asp.net/mvc/mvc4) projects. I ususally work following the [Code-First principle](http://weblogs.asp.net/scottgu/archive/2010/07/16/code-first-development-with-entity-framework-4.aspx), this let's you start with defining your models in plain classes and then let the Entity Framework create the database tables for you.

## Enabling Migrations

To enable migrations open the Package Manager Console (Tools -> Library Package Manager -> Package Manager Console) and enter the following command

	Enable-Migrations		