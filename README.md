dotnet-config2json
============

[![AppVeyor build status][appveyor-badge]](https://ci.appveyor.com/project/andrewlock/dotnet-config2json/branch/master)

[appveyor-badge]: https://img.shields.io/appveyor/ci/andrewlock/dotnet-config2json/master.svg?label=appveyor&style=flat-square

[![NuGet][main-nuget-badge]][main-nuget] [![MyGet][main-myget-badge]][main-myget]

[main-nuget]: https://www.nuget.org/packages/dotnet-config2json/
[main-nuget-badge]: https://img.shields.io/nuget/v/dotnet-config2json.svg?style=flat-square&label=nuget
[main-myget]: https://www.myget.org/feed/andrewlock-ci/package/nuget/dotnet-config2json
[main-myget-badge]: https://img.shields.io/www.myget/andrewlock-ci/vpre/dotnet-config2json.svg?style=flat-square&label=myget

A simple tool to convert a web.config file to an appsettings.json file.

## Installation

The latest release of dotnet-tinify requires the [2.1.300-rc1](https://www.microsoft.com/net/download/dotnet-core/sdk-2.1.300-rc1) .NET Core SDK or newer.
Once installed, run this command:

```
dotnet install tool --global dotnet-tinify
```

## Usage

```
Usage: dotnet config2json [arguments] [options]

Arguments:
  path          Path to the file or directory to migrate
  delimiter     The character in keys to replace with the section delimiter (:)
  prefix        If provided, an additional namespace to prefix on generated keys

Options:
  -?|-h|--help  Show help information

Performs basic migration of an xml .config file to
a JSON file. Uses the 'key' value as the key, and the
'value' as the value. Can optionally replace a given
character with the section marker (':').