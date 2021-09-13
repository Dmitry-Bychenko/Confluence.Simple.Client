# Confluence.Simple.Client

[![NuGet version (Confluence.Simple.Client)](https://img.shields.io/nuget/v/Confluence.Simple.Client.svg?style=flat-square)](https://www.nuget.org/packages/Confluence.Simple.Client/)

```c#

ConfluenceConnection conn = new ConfluenceConnection(
  "MyLogon",
  "MyPassword",
  "https://confluence-example.com/");

var q = conn.CreateQuery();
     
await foreach(var jsonDoc in q.QueryPagedAsync("api : space")) {
  using (jsonDoc) {
    //TODO: read Json doc here
  }
}

```
