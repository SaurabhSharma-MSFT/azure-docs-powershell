---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: 
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/ServiceBus/ServiceBus/help/Deny-AzServiceBusPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/ServiceBus/ServiceBus/help/Deny-AzServiceBusPrivateEndpointConnection.md
---

# Deny-AzServiceBusPrivateEndpointConnection

## SYNOPSIS
Rejects a private endpoint connection for an Service Bus namespace.

## SYNTAX

### PrivateEndpointPropertiesSet (Default)
```
Deny-AzServiceBusPrivateEndpointConnection [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-Name] <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### PrivateEndpointResourceIdParameterSet
```
Deny-AzServiceBusPrivateEndpointConnection [-ResourceId] <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Rejects a private endpoint connection for an Service Bus namespace.

## EXAMPLES

### Example 1
```powershell
PS C:\> Deny-AzServiceBusPrivateEndpointConnection -ResourceGroupName myresourcegroup -NamespaceName mynamespace -Name 00000000000
```

Denies a private endpoint connection `00000000000` to connect to Service Bus namespace `mynamespace`. 
Note that connection name is NOT the same as Private Endpoint Name.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Description of the connection state.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Private Endpoint Connection Name.

```yaml
Type: System.String
Parameter Sets: PrivateEndpointPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
ServiceBus Namespace Name.

```yaml
Type: System.String
Parameter Sets: PrivateEndpointPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resource Group Name

```yaml
Type: System.String
Parameter Sets: PrivateEndpointPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Private Endpoint Connection ResourceId.

```yaml
Type: System.String
Parameter Sets: PrivateEndpointResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusPrivateEndpointConnectionAttributes

## NOTES

## RELATED LINKS
