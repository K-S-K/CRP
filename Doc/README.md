# CRP
Content Representation Platform


#### Originating Projects Infrastructure by CLI

[dotnet new <TEMPLATE>](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-new)



dotnet new sln --name CRP

dotnet new classlib -o CRP.Common
dotnet sln add CRP.Common/CRP.Common.csproj 

dotnet new web -o CRP.Content
dotnet sln add CRP.Content/CRP.Content.csproj

dotnet new blazor -o CRP.Site
dotnet sln add CRP.Site/CRP.Site.csproj

dotnet new xunit -o CRP.Tests
dotnet sln add CRP.Tests/CRP.Tests.csproj

dotnet add CRP.Site/CRP.Site.csproj reference CRP.Common/CRP.Common.csproj 
dotnet add CRP.Tests/CRP.Tests.csproj reference CRP.Common/CRP.Common.csproj 
dotnet add CRP.Content/CRP.Content.csproj reference CRP.Common/CRP.Common.csproj 

