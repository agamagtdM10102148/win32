---
Description: 'The Win32\_LogicalFileSecuritySetting&\#32;WMI class represents security settings for a logical file. You cannot enumerate instances of this class.'
audience: developer
author: 'REDMOND\\markl'
manager: 'REDMOND\\markl'
ms.assetid: '3af570e7-74fb-4bb0-9c45-b718d471351d'
ms.prod: 'windows-server-dev'
ms.technology: 'windows-management-instrumentation'
ms.tgt_platform: multiple
title: 'Win32\_LogicalFileSecuritySetting class'
---

# Win32\_LogicalFileSecuritySetting class

The **Win32\_LogicalFileSecuritySetting** [WMI class](https://msdn.microsoft.com/library/aa393244) represents security settings for a logical file. You cannot enumerate instances of this class.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties. Properties are listed in alphabetic order, not MOF order.

## Syntax

``` syntax
[Dynamic, Provider("SECRCW32"), UUID("{8502C58C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalFileSecuritySetting : Win32_SecuritySetting
{
  string� Caption;
  string� Description;
  string� SettingID;
  uint32� ControlFlags;
  boolean OwnerPermissions;
  string� Path;
};
```

## Members

The **Win32\_LogicalFileSecuritySetting** class has these types of members:

-   [Methods](#methods)
-   [Properties](#properties)

### Methods

The **Win32\_LogicalFileSecuritySetting** class has these methods.



| Method                                                                                                  | Description                                                                                                |
|:--------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting.md) | Class method that retrieves a structural representation of the object security descriptor (SD).<br/> |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting.md) | Class method that sets an SD to the specified structure.<br/>                                        |



�

### Properties

The **Win32\_LogicalFileSecuritySetting** class has these properties.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MaxLen**](https://msdn.microsoft.com/library/aa393650) (64)
</dt> </dl>

Short textual description of the [**CIM\_Setting**](https://msdn.microsoft.com/library/aa388461) object.

This property is inherited from [**CIM\_Setting**](https://msdn.microsoft.com/library/aa388461).

</dd> <dt>

**ControlFlags**
</dt> <dd> <dl> <dt>

Data type: **uint32**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Control bits that qualify the meaning of an SD or its individual members. For more information about how to set the **ControlFlags** value, see the Remarks section. The following list lists the flags in **ControlFlags**. For more information, see [**SECURITY\_DESCRIPTOR\_CONTROL**](https://msdn.microsoft.com/library/windows/desktop/aa379566).

This property is inherited from [**Win32\_SecuritySetting**](win32-securitysetting.md).

<dt>

<span id="SE_OWNER_DEFAULTED"></span><span id="se_owner_defaulted"></span>

<span id="SE_OWNER_DEFAULTED"></span><span id="se_owner_defaulted"></span>**SE\_OWNER\_DEFAULTED** (1 (0x1))


</dt> <dd>

Indicates an SD with a default owner security identifier (SID). You can use this bit to find all of the objects that have default owner permissions set.

</dd> <dt>

<span id="SE_GROUP_DEFAULTED"></span><span id="se_group_defaulted"></span>

<span id="SE_GROUP_DEFAULTED"></span><span id="se_group_defaulted"></span>**SE\_GROUP\_DEFAULTED** (2 (0x2))


</dt> <dd>

Indicates an SD with a default group SID. You can use this bit to find all of the objects that have default group permissions set.

</dd> <dt>

<span id="SE_DACL_PRESENT"></span><span id="se_dacl_present"></span>

<span id="SE_DACL_PRESENT"></span><span id="se_dacl_present"></span>**SE\_DACL\_PRESENT** (4 (0x4))


</dt> <dd>

Indicates an SD that has a discretionary access control list (DACL). If this flag is not set, or if this flag is set and the DACL is **NULL**, the SD allows full access to everyone.

</dd> <dt>

<span id="SE_DACL_DEFAULTED"></span><span id="se_dacl_defaulted"></span>

<span id="SE_DACL_DEFAULTED"></span><span id="se_dacl_defaulted"></span>**SE\_DACL\_DEFAULTED** (8 (0x8))


</dt> <dd>

Indicates an SD with a default DACL. For example, if an object creator does not specify a DACL, the object receives the default DACL from the access token of the creator. This flag can affect how the system treats the DACL, with respect to access control entry (ACE) inheritance. The system ignores this flag if the **SE\_DACL\_PRESENT** flag is not set.

</dd> <dt>

<span id="SE_SACL_PRESENT"></span><span id="se_sacl_present"></span>

<span id="SE_SACL_PRESENT"></span><span id="se_sacl_present"></span>**SE\_SACL\_PRESENT** (16 (0x10))


</dt> <dd>

Indicates an SD that has a system access control list (SACL).

</dd> <dt>

<span id="SE_SACL_DEFAULTED"></span><span id="se_sacl_defaulted"></span>

<span id="SE_SACL_DEFAULTED"></span><span id="se_sacl_defaulted"></span>**SE\_SACL\_DEFAULTED** (32 (0x20))


</dt> <dd>

Indicates an SD with a default SACL. For example, if an object creator does not specify an SACL, the object receives the default SACL from the access token of the creator. This flag can affect how the system treats the SACL, with respect to ACE inheritance. The system ignores this flag if the **SE\_SACL\_PRESENT** flag is not set.

</dd> <dt>

<span id="SE_DACL_AUTO_INHERIT_REQ"></span><span id="se_dacl_auto_inherit_req"></span>

<span id="SE_DACL_AUTO_INHERIT_REQ"></span><span id="se_dacl_auto_inherit_req"></span>**SE\_DACL\_AUTO\_INHERIT\_REQ** (256 (0x100))


</dt> <dd>

Requests that the provider for the object protected by the SD automatically propagate the DACL to existing child objects. If the provider supports automatic inheritance, it propagates the DACL to any existing child objects, and sets the **SE\_DACL\_AUTO\_INHERITED** bit in the security descriptors of the object and its child objects.

</dd> <dt>

<span id="SE_SACL_AUTO_INHERIT_REQ"></span><span id="se_sacl_auto_inherit_req"></span>

<span id="SE_SACL_AUTO_INHERIT_REQ"></span><span id="se_sacl_auto_inherit_req"></span>**SE\_SACL\_AUTO\_INHERIT\_REQ** (512 (0x200))


</dt> <dd>

Requests that the provider for the object protected by the SD automatically propagate the SACL to existing child objects. If the provider supports automatic inheritance, it propagates the SACL to any existing child objects, and sets the **SE\_SACL\_AUTO\_INHERITED** bit in the SDs of the object and its child objects.

</dd> <dt>

<span id="SE_DACL_AUTO_INHERITED"></span><span id="se_dacl_auto_inherited"></span>

<span id="SE_DACL_AUTO_INHERITED"></span><span id="se_dacl_auto_inherited"></span>**SE\_DACL\_AUTO\_INHERITED** (1024 (0x400))


</dt> <dd>

Windows�2000 only. Indicates an SD in which the DACL is set up to support automatic propagation of inheritable ACEs to existing child objects. The system sets this bit when it performs the automatic inheritance algorithm for the object and its existing child objects. This bit is not set in SDs for Windows�NT versions 4.0 and earlier, which do not support automatic propagation of inheritable ACEs.

</dd> <dt>

<span id="SE_SACL_AUTO_INHERITED"></span><span id="se_sacl_auto_inherited"></span>

<span id="SE_SACL_AUTO_INHERITED"></span><span id="se_sacl_auto_inherited"></span>**SE\_SACL\_AUTO\_INHERITED** (2048 (0x800))


</dt> <dd>

Windows�2000: Indicates an SD in which the SACL is set up to support automatic propagation of inheritable ACEs to existing child objects. The system sets this bit when it performs the automatic inheritance algorithm for the object and its existing child objects. This bit is not set in SDs for Windows�NT versions 4.0 and earlier, which do not support automatic propagation of inheritable ACEs.

</dd> <dt>

<span id="SE_DACL_PROTECTED"></span><span id="se_dacl_protected"></span>

<span id="SE_DACL_PROTECTED"></span><span id="se_dacl_protected"></span>**SE\_DACL\_PROTECTED** (4096 (0x1000))


</dt> <dd>

Windows�2000: Prevents the DACL of the SD from being modified by inheritable ACEs.

</dd> <dt>

<span id="SE_SACL_PROTECTED"></span><span id="se_sacl_protected"></span>

<span id="SE_SACL_PROTECTED"></span><span id="se_sacl_protected"></span>**SE\_SACL\_PROTECTED** (8192 (0x2000))


</dt> <dd>

Windows�2000: Prevents the SACL of the SD from being modified by inheritable ACEs.

</dd> <dt>

<span id="SE_SELF_RELATIVE"></span><span id="se_self_relative"></span>

<span id="SE_SELF_RELATIVE"></span><span id="se_self_relative"></span>**SE\_SELF\_RELATIVE** (32768 (0x8000))


</dt> <dd>

Indicates an SD in self-relative format with all of the security information in a contiguous block of memory. If this flag is not set, the SD is in absolute format. For more information, see [Absolute and Self-Relative Security Descriptors](https://msdn.microsoft.com/library/windows/desktop/aa374807).

</dd> </dl>

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Textual description of the [**CIM\_Setting**](https://msdn.microsoft.com/library/aa388461) object.

This property is inherited from [**CIM\_Setting**](https://msdn.microsoft.com/library/aa388461).

</dd> <dt>

**OwnerPermissions**
</dt> <dd> <dl> <dt>

Data type: **boolean**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Owner permissions to the object.

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**key**](https://msdn.microsoft.com/library/aa392157)
</dt> </dl>

Full path of the file or directory.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MaxLen**](https://msdn.microsoft.com/library/aa393650) (256)
</dt> </dl>

Identifier by which the [**CIM\_Setting**](https://msdn.microsoft.com/library/aa388461) object is known.

This property is inherited from [**CIM\_Setting**](https://msdn.microsoft.com/library/aa388461).

</dd> </dl>

## Remarks

The **Win32\_LogicalFileSecuritySetting** class is derived from [**Win32\_SecuritySetting**](win32-securitysetting.md).

The **ControlFlags** property contains individual bit positions that identify the specific flags that are set. You can combine the flags by adding the associated values. For example, to specify both **SE\_DACL\_PRESENT** and **SE\_DACL\_AUTO\_INHERITED** you add the associated values 4 and 1024 to make the value of the **ControlFlags** property 1028.

If the **SE\_DACL\_PRESENT** bit is specified and a DACL entry is also present in the call to [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting.md), an empty DACL is written out. If the **SE\_DACL\_PRESENT** bit is not set in the control flags, but a DACL is specified as being written out, none will be. Conversely, if **SE\_DACL\_PRESENT** bit is set, but no actual DACL parameter is set when calling **SetSecurityDescriptor**, a **NULL** DACL is written out.

> [!Note]  
> A **NULL** DACL creates a security risk because it gives full access to everyone. For more information, see [Creating a DACL](https://msdn.microsoft.com/library/windows/desktop/ms717798).

�

If the **SeSecurityPrivilege** is not granted or enabled, then the SACL is not returned. For more information, see [**Privilege Constants**](https://msdn.microsoft.com/library/aa392758) and [Executing Privileged Operations](https://msdn.microsoft.com/library/aa390428).

## Examples

The following VBScript code example obtains a **Win32\_LogicalFileSecuritySetting** instance for file C:\\Temp on the local computer.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

Set colItems = objWMIService.ExecQuery( _
    "SELECT * FROM Win32_LogicalFileSecuritySetting WHERE Path=""c:\\Temp""",,48) 
For Each objItem in colItems 
    Wscript.Echo "Win32_LogicalFileSecuritySetting for file c:\Temp"
    Wscript.Echo "ControlFlags: " & objItem.ControlFlags
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "OwnerPermissions: " & objItem.OwnerPermissions
    Wscript.Echo "Path: " & objItem.Path
    Wscript.Echo "SettingID: " & objItem.SettingID
Next
```



## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server�2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Secrcw32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[**Win32\_SecuritySetting**](win32-securitysetting.md)
</dt> <dt>

[Operating System Classes](https://msdn.microsoft.com/library/aa392727)
</dt> <dt>

[Changing Access Security on Securable Objects](https://msdn.microsoft.com/library/aa384905)
</dt> <dt>

[WMI Security Descriptor Objects](https://msdn.microsoft.com/library/aa394577)
</dt> </dl>

�

�



