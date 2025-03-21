---
external help file: VMDirectStorage-help.xml
Module Name: VMDirectStorage
ms.date: 03/21/2025
online version: https://learn.microsoft.com/powershell/module/vmdirectstorage/remove-vmdirectvirtualdisk?view=windowsserver2025-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Remove-VMDirectVirtualDisk
ai-usage: ai-generated
---

# Remove-VMDirectVirtualDisk

## SYNOPSIS

Removes a direct-attached virtual disk from a Hyper-V virtual machine.

## SYNTAX

### ByVMName

```
Remove-VMDirectVirtualDisk [-VMName] <String> [-CimSession <CimSession[]>] [-ControllerType] <ControllerType>
 [-ControllerNumber] <Int32> [-ControllerLocation] <Int32> [<CommonParameters>]
```

### ByVirtualDisk

```
Remove-VMDirectVirtualDisk [-VirtualDisk] <VMDirectVirtualDisk[]> [<CommonParameters>]
```

## DESCRIPTION

The Remove-VMDirectVirtualDisk cmdlet removes a direct-attached virtual disk from a specified Hyper-V virtual machine. You can specify the virtual disk directly or identify it by the virtual machine name and controller details.

## EXAMPLES

### Example 1

```powershell
$parameters = @{
    VMName = "VM01"
    ControllerType = "SCSI"
    ControllerNumber = 0
    ControllerLocation = 1
}
Remove-VMDirectVirtualDisk @parameters
```

This example removes the direct-attached virtual disk located on SCSI controller 0, location 0, from the virtual machine named VM01.

## PARAMETERS

### -CimSession

Specifies the CimSession used to run the cmdlet on a remote computer or session.

```yaml
Type: Microsoft.Management.Infrastructure.CimSession[]
Parameter Sets: ByVMName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControllerLocation

Specifies the location number of the controller where the virtual disk is attached.

```yaml
Type: System.Int32
Parameter Sets: ByVMName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControllerNumber

Specifies the number of the controller where the virtual disk is attached.

```yaml
Type: System.Int32
Parameter Sets: ByVMName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControllerType

Specifies the type of controller. Currently, only SCSI is supported.

```yaml
Type: ControllerType
Parameter Sets: ByVMName
Aliases:
Accepted values: SCSI

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualDisk

Specifies the VMDirectVirtualDisk object to remove.

```yaml
Type: VMDirectVirtualDisk[]
Parameter Sets: ByVirtualDisk
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMName

Specifies the name of the virtual machine from which the virtual disk is removed.

```yaml
Type: System.String
Parameter Sets: ByVMName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

You can pipe a virtual machine name to this cmdlet.

### VMDirectVirtualDisk[]

You can pipe VMDirectVirtualDisk objects to this cmdlet.

## OUTPUTS

### System.Object

This cmdlet returns an object representing the removed virtual disk.

## NOTES

## RELATED LINKS

[Add-VMDirectVirtualDisk](Add-VMDirectVirtualDisk.md)

[Get-VMDirectVirtualDisk](Get-VMDirectVirtualDisk.md)
