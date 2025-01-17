---
title: desktop10:TypeSupported
description: Specifies a supported event log type.
keywords: windows 10, uwp, schema, manifest, desktop, extension

ms.date: 05/23/2022
ms.topic: reference
---

# desktop10:TypeSupported

## Description

Specifies a supported event log type.

## Element hierarchy

<dl>
<dt><a href="element-package.md">&lt;Package&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-extensions.md">&lt;Extensions&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-desktop10-extension.md">&lt;desktop10:Extension&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-desktop10-customdesktopeventlog.md">&lt;desktop10:CustomDesktopEventLog&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-desktop10-customeventsource.md">&lt;desktop10:CustomEventSource&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-desktop10-eventmessagefiles.md">&lt;desktop10:TypesSupported&gt;</a></dt>
<dd><strong>&lt;desktop10:TypeSupported&gt;</strong></dd>
</dd>
</dl>
</dd>
</dl>
</dd>
</dl>
</dd>
</dl>
</dd>
</dl>

## Syntax

```xml
<desktop10:TypeSupported
  Value = A string value that can be one of the following: "auditFailure", "auditSuccess", "errorType", "informationType", or "warningType".
  >

</desktop10:TypeSupported>
```

### Key

`?` optional (zero or one)

## Attributes and elements

### Attributes

| Attribute | Description | Data type | Required |
|-|-|-|-|
| Value | The supported event log type. | A string value that can be one of the following: "auditFailure", "auditSuccess", "errorType", "informationType", or "warningType". | Yes |

### Child Elements

None.

### Parent Elements

| Parent element | Description |
|-|-|
| [desktop10:TypesSupported](element-desktop10-typessupported.md) | Defines 1 or more of the Eventlog types supported by the event source. |

## Remarks

For more information on event log types, see [Event Sources](/windows/win32/eventlog/event-sources).


## Requirements

| Namespace | Value |
|-|-|
| **desktop10** | `http://schemas.microsoft.com/appx/manifest/desktop/windows10/10` |