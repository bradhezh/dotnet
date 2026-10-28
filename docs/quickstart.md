---
title: QuickStart
slug: /
---

```bash
dotnet --version
dotnet --list-sdks

# Web
# Empty hello-world app
dotnet new web -o HelloWorld
# Minimal API by default, --use-controllers for a controller template
dotnet new webapi -o HelloWorld
cd HelloWorld
dotnet run
dotnet watch
dotnet dev-certs https --trust
sudo dotnet workload update

# GUI
dotnet new install Avalonia.Templates
dotnet new list avalonia
dotnet new avalonia.mvvm -o HelloWorld
cd HelloWorld
# Strip UTF-8 BOM and convert CRLF (^M) to LF
find . -type f \( -name "*.cs" -o -name "*.axaml" -o -name "*.csproj" -o -name "*.manifest" \) -exec sed -i '' $'1s/^\xEF\xBB\xBF//' {} + -exec sed -i '' 's/\r$//' {} +
dotnet run
dotnet add package Microsoft.Extensions.DependencyInjection
```
