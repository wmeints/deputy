# Deputy

Welcome to Deputy, a tool to centralize your package versions in a .NET
solution. 

## Why use Deputy?

Nuget provides a way to centralize the package version management. However,
to set this up you'll need to perform a couple of steps:

1. Create a `Directory.Packages.props` in the root of the solution.
2. Add `<PackageVersion>` entries to the packages file.
3. Remove the `Version="..."` property from the `<PackageReference>` csproj
   files.

If you're not familiar with this new feature, you learn about it on the
[Nuget blog][nuget_blog].

Converting your project to centralized package versioning can be quite a lot
of work. Deputy helps you to convert your project and automates the process
of keeping your package versions up-to-date as well.

## Features

Deputy provides a number of useful features:

* Convert projects to use centralized dependency versioning
* Upgrade package versions
* Manage package references with centralized version management

### Convert projects to use centralized dependency versioning

When you initialize Deputy on your project it will automatically convert your
solution to use centralized dependency versioning.

Using centralized package versioning makes it easier for teams to synchronize
the versions of the packages used throughout a codebase.

### Upgrade package versions

You can use Deputy to scan packages for newer versions and upgrade them as
necessary. Deputy can automatically create pull requests on Github, Gitlab, and
Azure DevOps for you.

You have the option to upgrade packages the latest major, minor or patch 
release.

### Manage package references with centralized version management

Once you have deputy installed you can manage packages with centralized
versioning using the deputy package commands. Using Deputy for package
management ensures that when you add a package, it's version is automatically
maintained in the centralized `Directory.Packages.props` file.

## Getting started

Follow these steps to get started with Deputy.
First, install the tool using the following command:

```shell
dotnet tool install -g deputy
```

After installing the tool, you can initialize deputy with the following command:

```shell
deputy init
```

This will create the `Directory.Packages.props` file and extract the package
versions from the csproj files in the subfolders and generate `<PackageVersion>`
entries in the `Directory.Packages.props` file.

## Documentation

This section provides basic documentation for the tool. Please review each
of the sections to learn more about specific commands.

### Managing package references

TODO: Describe how managing packages works with deputy.

### Updating package versions

TODO: Describe how updating package versions will work.

## Engineering

TODO: Describe the key information needed to edit the code of the project.

[nuget_blog]: https://devblogs.microsoft.com/nuget/introducing-central-package-management/