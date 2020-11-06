---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 13c2f20f6d8ef7823244c62cfbe97e4b3a25eb73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429154"
---
# Remove-AzureRmRecoveryServicesAsrNetworkMapping

## Sinopse
Exclui o mapeamento de rede ASR especificado do cofre de serviços de recuperação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmRecoveryServicesAsrNetworkMapping** exclui o mapeamento de rede ASR especificado.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

Inicia a exclusão do mapeamento de rede ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.

## OS

### -InputObject
O objeto de entrada para o cmdlet: o objeto de mapeamento de rede ASR correspondente ao mapeamento de rede ASR a ser excluído.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetworkMapping

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmRecoveryServicesAsrNetworkMapping](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[New-AzureRmRecoveryServicesAsrNetworkMapping](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
