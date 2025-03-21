---
external help file: VMDirectStorage-help.xml
Module Name: VMDirectStorage
ms.date: 03/21/2025
online version: https://learn.microsoft.com/powershell/module/vmdirectstorage/add-vmdirectvirtualdisk?view=windowsserver2025-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Add-VMDirectVirtualDisk
ai-usage: ai-generated
---

# Add-VMDirectVirtualDisk

## SYNOPSIS

Adds a direct-attached virtual disk to a Hyper-V virtual machine.

## SYNTAX

### ByVMName

```
Add-VMDirectVirtualDisk [-VMName] <String[]> [-CimSession <CimSession[]>] [[-ControllerType] <ControllerType>]
 [[-ControllerNumber] <Int32>] [-ControllerLocation <Int32>] [-VirtualDiskUniqueId <String>]
 [<CommonParameters>]
```

### ByVM

```
Add-VMDirectVirtualDisk [-VM] <VirtualMachine[]> [[-ControllerType] <ControllerType>]
 [[-ControllerNumber] <Int32>] [-ControllerLocation <Int32>] [-VirtualDiskUniqueId <String>]
 [<CommonParameters>]
```

### ByVMDriveController

```
Add-VMDirectVirtualDisk [-VMDriveController] <VMDriveController> [-ControllerLocation <Int32>]
 [-VirtualDiskUniqueId <String>] [<CommonParameters>]
```

## DESCRIPTION

The Add-VMDirectVirtualDisk cmdlet attaches a direct-attached virtual disk to a Hyper-V virtual machine. You can specify the virtual machine by name, by virtual machine object, or by VM drive controller. You can also specify the unique identifier of the virtual disk to attach.

## EXAMPLES

### Example 1

```powershell
$parameters = @{
    VMName = "VM01"
    ControllerType = "SCSI"
    ControllerNumber = 0
    ControllerLocation = 1
    VirtualDiskUniqueId = "12345678-1234-1234-1234-123456789abc"
}
Add-VMDirectVirtualDisk @parameters
```

This example attaches a direct-attached virtual disk identified by its unique ID to the virtual machine named "VM01" at the specified SCSI controller location.

## PARAMETERS

### -CimSession

Specifies the CimSession used for remote management.

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

Specifies the location number on the controller to attach the virtual disk.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControllerNumber

Specifies the number of the controller to attach the virtual disk.

```yaml
Type: System.Int32
Parameter Sets: ByVMName, ByVM
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControllerType

Specifies the type of controller. Currently, only SCSI is supported.

```yaml
Type: ControllerType
Parameter Sets: ByVMName, ByVM
Aliases:
Accepted values: SCSI

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualDiskUniqueId

Specifies the unique identifier (GUID) of the virtual disk to attach.

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

### -VM

Specifies the virtual machine object to which the virtual disk is attached.

```yaml
Type: Microsoft.HyperV.PowerShell.VirtualMachine[]
Parameter Sets: ByVM
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMDriveController

Specifies the VM drive controller object to which the virtual disk is attached.

```yaml
Type: Microsoft.HyperV.PowerShell.VMDriveController
Parameter Sets: ByVMDriveController
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMName

Specifies the name of the virtual machine to which the virtual disk is attached.

```yaml
Type: System.String[]
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

### System.String[]

Accepts virtual machine names as input.

### Microsoft.HyperV.PowerShell.VirtualMachine[]

Accepts Hyper-V virtual machine objects.

### Microsoft.HyperV.PowerShell.VMDriveController

Accepts VM drive controller objects.

## OUTPUTS

### System.Object

Returns an object representing the attached virtual disk.

## NOTES

## RELATED LINKS

[Get-VMDirectVirtualDisk](Get-VMDirectVirtualDisk.md)

[Remove-VMDirectVirtualDisk](Remove-VMDirectVirtualDisk.md)
