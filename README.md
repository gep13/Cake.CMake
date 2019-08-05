# Cake.CMake
[![Nuget](https://img.shields.io/nuget/v/Cake.CMake.svg)](https://www.nuget.org/packages/Cake.CMake)

Addin that extends Cake with CMake support.

# How to use

## For to generate 
```csharp
#addin nuget:?package=Cake.CMake

Task("CMake")
    .Does(() =>
{
    var settings = new CMakeSettings
    {
        OutputPath = "path/to/build",
        SourcePath = "path/to/source"
    };
    
    CMake(settings);
});

```
## For to build 
```csharp
#addin nuget:?package=Cake.CMake

Task("CMake")
    .Does(() =>
{
    var settings = new CMakeBuildSettings
    {
        BinaryPath = "path/to/build"
    };
    
    CMakeBuild(settings);
});

```
