---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
---

# Get-AzCdnEndpoint

## SYNOPSIS
Gets a CDN endpoint.

> [!NOTE]
>This is the previous version of our documentation. Please consult [the most recent version](/powershell/module/az.cdn/get-azcdnendpoint) for up-to-date information.

## SYNTAX

### ByFieldsParameterSet (Default)
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectParameterSet
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.

## EXAMPLES

### Example 1: Get all endpoints in the CDN profile
```powershell
Get-AzCdnEndpoint -ResourceGroupName myresourcegroup -ProfileName mycdnprofile
```

```Output
HostName                   : myendpoint.azureedge.net
OriginHostHeader           :
OriginPath                 :
ContentTypesToCompress     : {}
IsCompressionEnabled       : False
IsHttpAllowed              : True
IsHttpsAllowed             : True
QueryStringCachingBehavior : IgnoreQueryString
Origins                    : {mystorage}
OptimizationType           :
ProbePath                  :
GeoFilters                 : {}
DeliveryPolicy             :
ResourceState              : Running
DefaultOriginGroup         :
ResourceGroupName          : myresourcegroup
ProfileName                : mycdnprofile
Location                   : WestUs
Tags                       : {}
Id                         : /subscriptions/11111111-1111-1111-1111-111111111111/resourcegroups/myresourcegroup/providers/Micr
                             osoft.Cdn/profiles/mycdnprofile/endpoints/myendpoint
Name                       : myendpoint
Type                       : Microsoft.Cdn/profiles/endpoints
ProvisioningState          : Succeeded
```

## PARAMETERS

### -CdnProfile
Specifies the CDN profile object to which the endpoint belongs.

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with azure

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

### -EndpointName
Specifies the name of the endpoint.
The name of the endpoint is not the host name of the endpoint.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
Specifies the name of the profile to which the endpoint belongs.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the resource group to which the endpoint belongs.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
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

### Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile

## OUTPUTS

### Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint

## NOTES

## RELATED LINKS

[New-AzCdnEndpoint](./New-AzCdnEndpoint.md)

[Remove-AzCdnEndpoint](./Remove-AzCdnEndpoint.md)

[Set-AzCdnEndpoint](./Set-AzCdnEndpoint.md)

[Start-AzCdnEndpoint](./Start-AzCdnEndpoint.md)

[Stop-AzCdnEndpoint](./Stop-AzCdnEndpoint.md)


