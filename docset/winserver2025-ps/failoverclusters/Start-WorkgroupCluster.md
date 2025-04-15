---
description: Starts a workgroup cluster.
external help file: Microsoft.FailoverClusters.Adless.PowerShell.psm1-help.xml
Module Name: FailoverClusters
ms.date: 04/15/2025
online version: https://learn.microsoft.com/powershell/module/failoverclusters/start-workgroupcluster?view=windowsserver2025-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Start-WorkgroupCluster
---

# Start-WorkgroupCluster

## SYNOPSIS
Starts a workgroup cluster.

## SYNTAX

```
Start-WorkgroupCluster [[-Node] <String[]>] [[-Credentials] <PSCredential[]>] [-IgnorePersistentState]
 [-AuthenticationMethod] <WorkgroupClusterAuthenticationMethod> [<CommonParameters>]
```

## DESCRIPTION
The Start-WorkgroupCluster function starts a workgroup cluster.

## PARAMETERS

### -AuthenticationMethod
Specifies the authentication method for the workgroup cluster.

```yaml
Type: WorkgroupClusterAuthenticationMethod
Parameter Sets: (All)
Aliases:
Accepted values: Certificates, NoCertificates

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credentials
An array of credentials for the nodes.

```yaml
Type: PSCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnorePersistentState
Indicates whether to ignore the persistent state of the cluster.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Node
An array of nodes that form the current cluster.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: @()
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EXAMPLES

### Example 1
```
Start-WorkgroupCluster -Node "Node1", "Node2" -Credentials $cred1, $cred2
```

This example starts the cluster.

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS