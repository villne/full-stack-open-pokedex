11.1 Warming up
Web API with C# .NET Core in Azure pipeline

Linting: I would use Roslyn analyzers. You can make Build Quality Checks in Azure, for eg. task to check warnings. In the project solution file, you can force analyzer packages to the whole project. The dotnet format can be set up to check or fix code violations and make the Azure pipeline fail.

Testing: I would use xUnit.net. In Azure you can make Visual Studio Test task where you define test files and generate Publish Test Results.

Building: I would use dotnet build to build the project.

I would choose Azure pipeline to automatically build and test your .NET Core projects.
Other good alternatives would be Google Cloud Build and AWS CodePipeline which offers CI pipelines.

The project is web API, hosting in a cloud-based environment would be the best option. Better scaling in the cloud.
