---
Description: 'WMI events are delivered by the event provider to a temporary or permanent consumer. The WMI event system uses the comparison of security descriptors on events and user account SIDs to control event access.'
audience: developer
author: 'REDMOND\\markl'
manager: 'REDMOND\\markl'
ms.assetid: '86eaeb5c-c27e-4794-88e2-e0ffbb885290'
ms.prod: 'windows-server-dev'
ms.technology: 'windows-management-instrumentation'
ms.tgt_platform: multiple
title: Securing WMI Events
---

# Securing WMI Events

WMI events are delivered by the [*event provider*](gloss-e.md#wmi-gloss-event-provider) to a [*temporary*](gloss-t.md#wmi-gloss-temporary-consumer) or [*permanent*](gloss-p.md#wmi-gloss-permanent-consumer) consumer. The WMI event system uses the comparison of [*security descriptors*](gloss-s.md#wmi-gloss-security-descriptor) on events and user account [*SIDs*](gloss-s.md#wmi-gloss-sid) to control event access.

Events are delivered in the form of an instance of an event class usually, but not necessarily, derived ultimately from [**\_\_Event**](--event.md). WMI supplies several general event classes in the [WMI System Classes](wmi-system-classes.md), such as [**\_\_InstanceModificationEvent**](--instancemodificationevent.md). Providers may also supply their own event classes. For example, the [System Registry Provider](https://msdn.microsoft.com/library/aa393886) has event classes that report the change of a registry key or value, such as [**RegistryKeyChangeEvent**](https://msdn.microsoft.com/library/aa393040).

The following topics supply information about securing delivery of events for providers and receiving events securely for client scripts and applications:

-   [Providing Events Securely](providing-events-securely.md)
-   [Receiving Events Securely](receiving-events-securely.md)

## Related topics

<dl> <dt>

[Maintaining WMI Security](maintaining-wmi-security.md)
</dt> </dl>

 

 


