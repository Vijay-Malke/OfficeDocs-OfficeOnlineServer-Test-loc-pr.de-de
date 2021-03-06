﻿---
title: New-SPWOPISuppressionSetting
TOCTitle: New-SPWOPISuppressionSetting
ms:assetid: 7e6bb8f5-3124-4568-80c6-02cae46b803b
ms:mtpsurl: https://technet.microsoft.com/de-de/library/JJ219443(v=office.15)
ms:contentKeyID: 49633167
ms.date: 12/22/2017
mtps_version: v=office.15
ms.translationtype: HT
---

# New-SPWOPISuppressionSetting

 

_**Gilt für:**Office Web Apps, SharePoint Foundation 2013, SharePoint Server 2013_

_**Letztes Änderungsdatum des Themas:**2015-03-09_

Das **New-SPWOPISuppressionSetting**-Cmdlet deaktiviert Office Web Apps für die Aktion, Dateinamenerweiterung oder Programmkennung, die Sie in der aktuellen SharePoint-Farm angegeben haben.

## Syntax

    New-SPWOPISuppressionSetting [-Action <String>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-Extension <String>] [-ProgId <String>] [-WhatIf [<SwitchParameter>]]

## Detaillierte Beschreibung

Das **New-SPWOPISuppressionSetting**-Cmdlet deaktiviert Office Web Apps für die Aktion, Dateinamenerweiterung oder Programmkennung ProgId(), die Sie in der aktuellen SharePoint-Farm angegeben haben. Das Cmdlet entfernt dabei nicht die Suchinformationen oder die Möglichkeit für Benutzer, die SharePoint-Funktion zum Freigeben mit Links zu verwenden, um einen Link an ein Dokument zu senden bzw. für den Empfänger, Office Web Apps zum Anzeigen dieses Dokumenttyps zu verwenden. Möglicherweise müssen Sie dieses Cmdlet verwenden, wenn Sie Excel Services anstatt der WOPI-Anwendung (z. B. Office Web Apps Server) zum Anzeigen von Excel-Arbeitsmappen verwenden möchten.

SharePoint-Verwaltungsshell

## Parameter


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Erforderlich</th>
<th>Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Action</strong></p></td>
<td><p>Optional</p></td>
<td><p>System.String</p></td>
<td><p>Gibt die zu unterdrückende Aktion für eine bestimmte Erweiterung oder Programmkennung (ProgId) an, z. B. “view”, “edit” und “embedview”. Führen Sie <strong>Get-SPWOPIBinding</strong> aus, um eine vollständige Liste mit Aktionen zu erhalten.</p></td>
</tr>
<tr class="even">
<td><p><strong>AssignmentCollection</strong></p></td>
<td><p>Optional</p></td>
<td><p>Microsoft.SharePoint.PowerShell.SPAssignmentCollection</p></td>
<td><p>Verwaltet Objekte zum Zweck der ordnungsgemäßen Beseitigung. Die Verwendung von Objekten wie beispielsweise <strong>SPWeb</strong> oder <strong>SPSite</strong> kann sehr viel Arbeitsspeicher erfordern, und für die Verwendung dieser Objekte in Windows PowerShell-Skripts muss der Arbeitsspeicher entsprechend verwaltet werden. Mit dem <strong>SPAssignment</strong>-Objekt können Sie einer Variablen Objekte zuweisen und die Objekte beseitigen, wenn sie nicht mehr benötigt werden, um Arbeitsspeicher freizugeben. Wenn die Objekte <strong>SPWeb</strong>, <strong>SPSite</strong> oder<strong>SPSiteAdministration</strong> verwendet werden, werden diese automatisch beseitigt, falls keine Zuweisungsauflistung oder kein <strong>Global</strong>-Parameter verwendet wird.</p>
<div class="alert">

> [!TIP]
> Wenn der <STRONG>Global</STRONG>-Parameter verwendet wird, sind alle Objekte im globalen Speicher enthalten. Es kann vorkommen, dass nicht genügend Arbeitsspeicher vorhanden ist, falls Objekte nicht sofort verwendet werden oder mit dem Befehl <STRONG>Stop-SPAssignment</STRONG> beseitigt werden.


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Confirm</strong></p></td>
<td><p>Optional</p></td>
<td><p>System.Management.Automation.SwitchParameter</p></td>
<td><p>Fordert Sie vor der Ausführung eines Befehls zur Bestätigung auf. Um weitere Informationen zu erhalten, geben Sie den folgenden Befehl ein: <strong>get-help about_commonparameters</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Extension</strong></p></td>
<td><p>Optional</p></td>
<td><p>System.String</p></td>
<td><p>Gibt die zu unterdrückende Dateinamenerweiterung an. Führen Sie Get-SPWOPIBinding aus, um die Liste mit von der WOPI-Anwendung unterstützten Dateinamenerweiterungen zu erhalten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ProgId</strong></p></td>
<td><p>Optional</p></td>
<td><p>System.String</p></td>
<td><p>Gibt die zu unterdrückende Programmkennung (ProgID) für eine Anwendung an. Führen Sie &quot;Get-SPWOPIBinding&quot; aus, um die Liste mit von der WOPI-Anwendung unterstützten ProgIds zu erhalten.</p></td>
</tr>
<tr class="even">
<td><p><strong>WhatIf</strong></p></td>
<td><p>Optional</p></td>
<td><p>System.Management.Automation.SwitchParameter</p></td>
<td><p>Zeigt eine Meldung an, die die Auswirkung des Befehls beschreibt, anstatt den Befehl auszuführen. Um weitere Informationen zu erhalten, geben Sie den folgenden Befehl ein: <strong>get-help about_commonparameters</strong>.</p></td>
</tr>
</tbody>
</table>


## Eingabetypen

## Rückgabetypen

## Beispiel

\--------------BEISPIEL 1-----------------

    New-SPWOPISuppressionSetting -Extension "XLSX" -Action "view"

    New-SPWOPISuppressionSetting -Extension "XLS" -Action "view"

In diesem Beispiel wird die Möglichkeit eines Benutzers deaktiviert, Office Web Apps zum Anzeigen von Excel-Arbeitsmappen mit den Dateinamenerweiterungen ".xlsx” oder “.xls” zu verwenden.

## Siehe auch


[Get-SPWOPISuppressionSetting](get-spwopisuppressionsetting.md)  
[Remove-SPWOPISuppressionSetting](remove-spwopisuppressionsetting.md)  


[Inhaltsübersicht für Office Web Apps Server](content-roadmap-for-office-web-apps-server.md)  
[Verwenden von Office Web Apps mit SharePoint 2013](use-office-web-apps-with-sharepoint-2013.md)

