.NET (4.5) [![Build status](https://ci.appveyor.com/api/projects/status/dvk19mkf6ry0lock/branch/master)](https://ci.appveyor.com/project/i4004/acspnet-json/branch/master) Mono (3.8.0) [![Travis build status](https://travis-ci.org/i4004/AcspNet.Json.png?branch=master)](https://travis-ci.org/i4004/AcspNet.Json)

[![NuGet Status](http://nugetstatus.com/AcspNet.Json.png)](http://nugetstatus.com/packages/AcspNet.Json)
[![Nuget version](http://img.shields.io/badge/nuget-v1.0.3-blue.png)](https://www.nuget.org/packages/AcspNet.Json/)

---

AcspNet.Json
============

`AcspNet.Json` is a package which provides JSON controller response for controllers and JSON view model binder for [AcspNet web-framework](https://github.com/i4004/AcspNet).

Available at NuGet as [source package](https://www.nuget.org/packages/AcspNet.Json/)

### Using JSON controller response

Framework execution will be stopped and object will be parsed to JSON string and sent to client
```csharp
	public class MyController : Controller
	{
		public override ControllerResponse Invoke()
		{
			return new Json(myObj);
		}
	}
```

### Using JSON view model binder

Registering binder:
```csharp
public void Configuration(IAppBuilder app)
{
	...
	HttpModelHandler.RegisterModelBinder<JsonModelBinder>();

	app.UseAcspNet();
}
```
