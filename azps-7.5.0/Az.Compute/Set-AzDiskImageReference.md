---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/main/src/Compute/Compute/help/Set-AzDiskImageReference.md
---

# Set-AzDiskImageReference

## SYNOPSIS
Sets the image reference properties on a disk object.

> [!NOTE]
>This is the previous version of our documentation. Please consult [the most recent version](/powershell/module/az.compute/set-azdiskimagereference) for up-to-date information.

## SYNTAX

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.

## EXAMPLES

### Example 1
```powershell
$diskconfig = New-AzDiskConfig -Location "East US" -DiskSizeGB 10 -AccountType Premium_LRS -OsType Windows -CreateOption FromImage
$image = '/Subscriptions/00000000-0000-0000-0000-000000000000/Providers/Microsoft.Compute/Locations/westeurope/Publishers/MicrosoftWindowsDesktop/ArtifactTypes/VMImage/Offers/Windows-10/Skus/win10-21h2-avd-g2/Versions/19044.1526.220204'
$diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0
New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig
```

The first command creates a local disk object with size 10GB in Premium_LRS storage account type.  It also sets Windows OS type.
The second command sets the image id and the logical unit number 0 for the disk object.
The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with azure.

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

### -Disk
Specifies a local disk object.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Id
Specifies the ID of PIR or user image.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Specifies the logical unit number (LUN). If the disk is created from an image's data disk, this is an index that indicates which of the data disks in the image to use. For OS disks, this field is null.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
Shows what would happen if the cmdlet runs. The cmdlet is not run.

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

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk

### System.String

### System.Int32

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk

## NOTES

## RELATED LINKS
