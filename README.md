# Sample .NET 6 Azure Function with AAD authentication and authorization through middleware

Usage instructions:

1. Register app in your Azure AD with needed scopes, user roles and app roles
1. Rename local.settings.sample.json to local.settings.json
1. Put your Azure AD tenant id in the authority setting
1. Put your app client ID in the client ID setting

There are a couple reflection hacks here that are bound to break at some point if the internals change.
It was the only way I found to set the response status code from within a middleware since all the relevant classes are marked internal.

<u>2022/3/31 Update by @Herman-Wu </u>
I forked this project and changed the project type of the IsolatedFunctionAuth project from an Azure Functions project to a .Net library project so that we can reuse it in different Azure Functions projects. 
