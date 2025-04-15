---
description: Removes certificates issued by a specific issuer from the local machine and current user certificate stores.
external help file: Microsoft.FailoverClusters.Adless.PowerShell.psm1-help.xml
Module Name: FailoverClusters
ms.date: 04/15/2025
online version: https://learn.microsoft.com/powershell/module/failoverclusters/remove-workgroupclustercertificates?view=windowsserver2025-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Remove-WorkgroupClusterCertificates
---

# Remove-WorkgroupClusterCertificates

## SYNOPSIS
Removes certificates issued by a specific issuer from the local machine and current user certificate stores.

## SYNTAX

```
Remove-WorkgroupClusterCertificates [[-Authority] <String>] [-Force] [<CommonParameters>]
```

## DESCRIPTION
The Remove-WorkgroupClusterCertificates function removes certificates from the following certificate stores:
- Cert:\LocalMachine\My
- Cert:\LocalMachine\Local Cert Issuer
- Cert:\CurrentUser\My
- Cert:\CurrentUser\CA

Certificates are filtered for those issued by issuers starting with PKU2UAuthority.

## PARAMETERS

### -Authority
Specifies the issuer of the certificates to remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: PKU2UAuthority*
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Indicates whether to force the removal of certificates without prompting for confirmation.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EXAMPLES

### Example 1
```
Remove-WorkgroupClusterCertificates -Force
```

Removes all certificates issued by "CN=PKU2UAuthority*" from the certificate stores without prompting for confirmation.

### Example 2
```
Remove-WorkgroupClusterCertificates
```

Prompts for confirmation before removing each certificate issued by "CN=PKU2UAuthority*" from the certificate stores.

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS