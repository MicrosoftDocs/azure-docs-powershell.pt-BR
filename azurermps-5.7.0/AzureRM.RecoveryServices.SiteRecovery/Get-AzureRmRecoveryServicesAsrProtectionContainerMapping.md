---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 5d0d6bc894cd252ac36b4ceee312040a998b3857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428833"
---
# Get-AzureRmRecoveryServicesAsrProtectionContainerMapping

## Sinopse
Obtém mapeamentos de contêiner de proteção do Azure site Recovery.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByObject (padrão)
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** Obtém informações sobre o contêiner de proteção para mapeamentos de política de replicação (Associação) no cofre para o contêiner de proteção ASR especificado.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

Lista de mapeamentos de contêineres de proteção para contêiner.

### Exemplo 2
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

Obtém todos os mapeamentos de contêiner de proteção para o contêiner de proteção especificado.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do mapeamento de contêiner de proteção a obter.

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionContainer
Obter mapeamentos de contêiner de proteção correspondentes ao objeto contêiner de proteção ASR especificado.

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer

## EXIBE

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmRecoveryServicesAsrProtectionContainerMapping](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
