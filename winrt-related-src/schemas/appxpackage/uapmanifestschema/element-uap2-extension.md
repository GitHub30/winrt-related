---
description: Declares an extensibility point for the app (uap2:Extension).
title: uap2:Extension (Windows 10)

keywords: windows 10, uwp, schema, package, manifest
ms.topic: reference
ms.date: 03/28/2022

---

# uap2:Extension (Windows 10)

Declares an extensibility point for the app.

## Element Hierarchy

[ < Package > ](element-package.md)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[ < Applications > ](element-applications.md)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[ < Application > ](element-application.md)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[ < Extensions > ](element-1-extensions.md)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**< UAP2:Extension >**

## Syntax

```syntax
<uap2:Extension Category                              = "windows.webAccountProvider"
                Executable?                           = A string between 1 and 256 characters in length that must end with ".exe" and cannot contain these characters: <, >, :, ", |, ?, or *. It specifies the default executable for the extension. If not specified, the executable defined for the app is used.  If specified, the EntryPoint property is also used. If that EntryPoint property isn't specified, the EntryPoint defined for the app is used.
                EntryPoint?                           = A string between 1 and 256 characters in length, representing the  task handling the extension. This is normally the fully namespace-qualified name of a Windows Runtime type. If EntryPoint is not specified, the EntryPoint defined for the app is used instead.
                RuntimeType?                          = A string between 1 and 255 characters in length that cannot start or end with a period or contain these characters: <, >, :, ", /, \, |, ?, or *.
                StartPage?                            = A string between 1 and 256 characters in length that cannot contain these characters: <, >, :, ", |, ?, or *. 
                ResourceGroup?                        =  An alphanumeric string between 1 and 255 characters in length. Must begin with an alphabetic character.
                uap10:TrustLevel?                     = String value. Can be one of the following: "appContainer", "mediumIL".
                uap10:RuntimeBehavior?                = String value. Can be one of the following: "windowsApp", "packagedClassicApp", "win32App".
                uap10:HostId?                         = An alphanumeric string between 1 and 255 characters in length. Must begin with an alphabetic character.
                uap10:Parameters?                     = A string between 1 and 32767 characters in length with a non-whitespace character at its beginning and end.
                previewappcompat:CompatMode?          = A string value that can be one of the following: "classic", "modern".
                previewappcompat:Scope?               = A string value that can be one of the following: "user", "machine".
                uap11:Id?                             = A string between 1 and 256 characters in length.
                uap11:Subsystem?                      = A string value. Can be one of the following: "console", "windows".
                uap11:SupportsMultipleInstances?      = A boolean value.
                uap11:ResourceGroup?                  = An alphanumeric string between 1 and 255 characters in length. Must begin with an alphabetic character.
                uap11:CurrentDirectoryPath?           = A string between 1 and 256 characters in length that cannot contain these characters: <, >, :, ", |, ?, or *.
                uap11:Parameters?                     = A string between 1 and 32767 characters in length with a non-whitespace character at its beginning and end.
                desktop7:CompatMode                   = A string value that can be one of the following: "classic", "modern".
                desktop7:Scope                        = A string value that can be one of the following: "user", "machine".
  
                                >

<!-- Child Elements -->
( uap2:webAccountProvider? )
</uap2:Extension>
```

### Key

`?` optional (zero or one)

## Attributes

| Attribute | Description | Data Type | Required |
|-----------|-------------|-----------|----------|
| Category | The category of the extension. | One of the following: "windows.webAccountProvider". | Yes |
| Executable | The default launch executable. | A string between 1 and 256 characters in length that must end with ".exe" and cannot contain these characters: <, >, :, ", &#124;, ?, or *. It specifies the default executable for the extension. If not specified, the executable defined for the app is used.  If specified, the EntryPoint property is also used. If that EntryPoint property isn't specified, the EntryPoint defined for the app is used. | No |
| EntryPoint | The activatable class ID. | A string between 1 and 256 characters in length, representing the task handling the extension. This is normally the fully namespace-qualified name of a Windows Runtime type. If EntryPoint is not specified, the EntryPoint defined for the app is used instead. | No |
| RuntimeType | The runtime provider. This attribute is used typically when there are mixed frameworks in an app. | A string between 1 and 255 characters in length that cannot start or end with a period or contain these characters: <, >, :, ", /, \, &#124;, ?, or *. | No |
| StartPage | The web page that handles the extensibility point. | A string between 1 and 256 characters in length that cannot contain these characters: <, >, :, ", &#124;, ?, or *. | No |
| ResourceGroup | The logical container where resources are managed. | An alphanumeric string between 1 and 255 characters in length. | No |
| uap10:TrustLevel | Specifies the trust level of the extension. | String value. Can be one of the following: "appContainer", "mediumIL".  | No |
| uap10:RuntimeBehavior | Specifies the run time behavior of the extension. | String value. Can be one of the following: "windowsApp", "packagedClassicApp", "win32App".  | No |
| uap10:HostId | Specifies the app ID of the host app for the extension. | An alphanumeric string between 1 and 255 characters in length. Must begin with an alphabetic character.  | No |
| uap10:Parameters | Contains command line parameters to pass to the extension. Only supported for desktop apps that have package identity. | A string between 1 and 32767 characters in length with a non-whitespace character at its beginning and end.  | No |
| previewappcompat:CompatMode | Specifies the compatibility mode when viewing application previews. | A string value that can be one of the following: "classic", "modern". | No |
| previewappcompat:Scope | Contains paraeters to manipulate the scope used for application previews. | A string value that can be one of the following: "user", "machine". | No |
| uap11:Id | The unique identifier for the extensibility point. | A string between 1 and 256 characters in length. | No |
| uap11:Subsystem | Specifies the type of system the application will run on. | String value. Can be one of the following: "console", "windows". | No |
| uap11:SupportsMultipleInstances | Specifies whether or not the application supports multiple instances. | Boolean value. | No
| uap11:Resource Group | The logical container where resources are managed. | An alphanumeric string between 1 and 255 characters in length. | No |
| uap11:CurrentDirectoryPath | Specifies the current directory the of the extensibility point. | A string between 1 and 256 characters in length that cannot contain these characters: <, >, :, ", &#124;, ?, or *. | No |
| uap11:Parameters | Contains command line parameters to pass to the extension. Only supported for desktop apps that have package identity. | A string between 1 and 32767 characters in length with a non-whitespace character at its beginning and end.  | No |
| desktop7:CompatMode | Specifies the compatibility mode when viewing application previews. | A string value that can be one of the following: "classic", "modern". | No |
| desktop7:Scope | Contains paraeters to manipulate the scope used for application previews. | A string value that can be one of the following: "user", "machine". | No |

## Child Elements

| Child Element | Description |
|---------------|-------------|
| [uap2:WebAccountProvider](element-uap2-webaccountprovider.md) | Declares an app extensibility point of type windows.webAccountProvider. |

## Requirements

| Namespace | Manifest Path |
|-----------|---------------|
| **UAP2** | `http://schemas.microsoft.com/appx/manifest/uap/windows10/2`
| **desktop7** | `http://schemas/microsoft.com/appx/manifest/desktop/windows10/7` |
| **previewappcompat** | `http://schemas/microsoft.com/appx/manifest/preview/windows10/msixappcompatsupport/3` |
| **UAP10** | `http://schemas.microsoft.com/appx/manifest/uap/windows10/10`
| **UAP11** | `http://schemas.microsoft.com/appx/manifest/uap/windows10/11`