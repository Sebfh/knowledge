# Howto: Start a ASP.NET MVC4 Project

This document holds a summary of command and tricks I use when working on [ASP.NET MVC4](http://www.asp.net/mvc/mvc4) projects. I ususally work following the [Code-First principle](http://weblogs.asp.net/scottgu/archive/2010/07/16/code-first-development-with-entity-framework-4.aspx), this lets you start with defining your models in plain classes and then let the Entity Framework create the database tables for you.

## Enabling Migrations

To enable migrations open the Package Manager Console (Tools -> Library Package Manager -> Package Manager Console) and enter the following command

	Enable-Migrations

If you use more then one DBContext you must enable migrations on every DbContext seperatly

	Enable-Migrations -ContextTypeName YourNameSpace.Models.MenuDbContext

Enabling database migrations creates a new Migrations Folder in your Visual Studio Solution as well as an InitialCreate Target Migration that has both an Up and Down Migration.	

## Creating a Migration

	Add-Migration YouMigrationName

When you're finished creating you migrations you can update your database

	Update-Database

## Bugs

Running a ASP.NET MVC 4 application on a fresh IIS7 server wil not work. You need to add the following lines to your Web.config

	<system.webServer>
    <modules>
      <remove name="UrlRoutingModule-4.0" />
      <add name="UrlRoutingModule-4.0" type="System.Web.Routing.UrlRoutingModule" preCondition="" />
      <!-- any other modules you want to run in MVC e.g. FormsAuthentication, Roles etc. -->
    </modules>