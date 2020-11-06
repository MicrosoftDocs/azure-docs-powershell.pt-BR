---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 3f380110359668af5c1b506e1736d3ecc9f39b3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429157"
---
# Remove-AzureRmRecoveryServicesAsrFabric

## Sinopse
Exclui a malha de recuperação de site do Azure especificada do cofre de serviços de recuperação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmRecoveryServicesAsrFabric** remove a estrutura de recuperação de site do Azure especificada do cofre de serviços de recuperação.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

Inicia a exclusão da malha especificada e retorna o trabalho ASR usado para acompanhar a operação.

## OS

### -Force
Force o comando a ser executado sem fornecer um aviso adicional.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
O objeto de entrada para o cmdlet: o objeto de malha ASR correspondente à malha a ser excluída.

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirme
Especifique se a confirmação é necessária. Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.

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
Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.

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

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmRecoveryServicesAsrFabric](./Get-AzureRmRecoveryServicesAsrFabric.md)

[New-AzureRmRecoveryServicesAsrFabric](./New-AzureRmRecoveryServicesAsrFabric.md)
