---
title: QuickStart
slug: /
---

```bash
dotnet --version
dotnet --list-sdks
# Empty hello-world app
dotnet new web -o hello-world
# Minimal API by default
dotnet new webapi --use-controllers -o hello-world
cd hello-world
dotnet run
dotnet watch
dotnet dev-certs https --trust
sudo dotnet workload update
```
