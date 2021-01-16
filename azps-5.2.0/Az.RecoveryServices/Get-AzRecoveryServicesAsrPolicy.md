---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259144"
---
# Get-AzRecoveryServicesAsrPolicy

## Sinopse
Obtém políticas de replicação ASR.

## SYNTAX

### Padrão (padrão)
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzRecoveryServicesAsrPolicy** Obtém a lista de políticas de replicação do Azure site Recovery configuradas ou uma política de replicação específica por nome.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

Retorna a lista de políticas de replicação

### Exemplo 2
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

Retorna a política de replicação com o nome.

### Exemplo 3
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

Retorna a política de replicação com o nome amigável especificado.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.


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

### -FriendlyName
Especifica o nome amigável da política de replicação ASR.

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da política de replicação ASR.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy

## INFORMA

## LINKS RELACIONADOS

[New-AzRecoveryServicesAsrPolicy](./New-AzRecoveryServicesAsrPolicy.md)

[Remove-AzRecoveryServicesAsrPolicy](./Remove-AzRecoveryServicesAsrPolicy.md)
