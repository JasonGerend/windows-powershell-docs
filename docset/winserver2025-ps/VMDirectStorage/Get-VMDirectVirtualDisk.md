---
external help file: VMDirectStorage-help.xml
Module Name: VMDirectStorage
ms.date: 03/21/2025
online version: https://learn.microsoft.com/powershell/module/vmdirectstorage/get-vmdirectvirtualdisk?view=windowsserver2025-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Get-VMDirectVirtualDisk
ai-usage: ai-generated
---

# Get-VMDirectVirtualDisk

## SYNOPSIS

Retrieves information about direct-attached virtual disks associated with Hyper-V virtual machines.

## SYNTAX

### ByVMName

```
Get-VMDirectVirtualDisk [-VMName] <String[]> [-CimSession <CimSession[]>] [[-ControllerType] <ControllerType>]
 [[-ControllerNumber] <Int32>] [-ControllerLocation <Int32>] [<CommonParameters>]
```

### ByVM

```
Get-VMDirectVirtualDisk [-VM] <VirtualMachine[]> [[-ControllerType] <ControllerType>]
 [[-ControllerNumber] <Int32>] [-ControllerLocation <Int32>] [<CommonParameters>]
```

### ByVMDriveController

```
Get-VMDirectVirtualDisk [-VMDriveController] <VMDriveController[]> [-ControllerLocation <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION

The Get-VMDirectVirtualDisk cmdlet retrieves information about direct-attached virtual disks associated with Hyper-V virtual machines. You can specify the virtual machine by name, by virtual machine object, or by VM drive controller.

## EXAMPLES

### Example 1

```powershell
Get-VMDirectVirtualDisk -VMName "VM01"
```

This command retrieves all direct-attached virtual disks associated with the virtual machine named "VM01".

## PARAMETERS

### -CimSession

Specifies the CimSession to use for remote management.

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

Specifies the location number of the controller to filter the virtual disks.

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

Specifies the number of the controller to filter the virtual disks.

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

### -VM

Specifies the virtual machine object from which to retrieve virtual disks.

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

Specifies the VM drive controller object from which to retrieve virtual disks.

```yaml
Type: Microsoft.HyperV.PowerShell.VMDriveController[]
Parameter Sets: ByVMDriveController
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMName

Specifies the name of the virtual machine from which to retrieve virtual disks.

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

### Microsoft.HyperV.PowerShell.VMDriveController[]

Accepts VM drive controller objects.

## OUTPUTS

### System.Object

Returns objects representing direct-attached virtual disks.

## NOTES

## RELATED LINKS

[Add-VMDirectVirtualDisk](Add-VMDirectVirtualDisk.md)

[Remove-VMDirectVirtualDisk](Remove-VMDirectVirtualDisk.md)
