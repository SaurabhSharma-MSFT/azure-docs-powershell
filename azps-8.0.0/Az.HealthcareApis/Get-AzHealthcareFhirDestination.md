---
external help file: 
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/get-azhealthcarefhirdestination
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/HealthcareApis/help/Get-AzHealthcareFhirDestination.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/HealthcareApis/help/Get-AzHealthcareFhirDestination.md
---

# Get-AzHealthcareFhirDestination

## SYNOPSIS
Lists all FHIR destinations for the given IoT Connector

> [!NOTE]
>This is the previous version of our documentation. Please consult [the most recent version](/powershell/module/az.healthcareapis/get-azhealthcarefhirdestination) for up-to-date information.

## SYNTAX

```
Get-AzHealthcareFhirDestination -IotConnectorName <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIPTION
Lists all FHIR destinations for the given IoT Connector

## EXAMPLES

### Example 1: Lists all FHIR destinations for the given IoT Connector
```powershell
PS C:\> Get-AzHealthcareFhirDestination -IotConnectorName azpsiotconnector -ResourceGroupName azps_test_group -WorkspaceName azpshcws

Location Name                                          ResourceGroupName
-------- ----                                          -----------------
eastus2  azpshcws/azpsiotconnector/azpsfhirdestination azps_test_group
```

Lists all FHIR destinations for the given IoT Connector

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IotConnectorName
The name of IoT Connector resource.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
The name of the resource group that contains the service instance.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
The subscription identifier.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
The name of workspace resource.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.Models.Api20211101.IIotFhirDestination

## NOTES

ALIASES

## RELATED LINKS

