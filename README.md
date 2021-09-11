# Confluence.Simple.Client

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
