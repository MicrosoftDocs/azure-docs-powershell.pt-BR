---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: f8d55ec80c6120f2159969ae6a58a531bea50b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429151"
---
# Set-AzureRmRecoveryServicesAsrVaultContext

## Sinopse
Define o contexto do cofre de serviços de recuperação a ser usado para operações subsequentes do Azure site Recovery na sessão atual do PowerShell.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmRecoveryServicesAsrVaultContext** define o contexto do cofre do Azure site Recovery para outras operações.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

Define o contexto do cofre para o cofre de serviços de recuperação especificado para operações subsequentes de recuperação de site do Azure na sessão atual do PowerShell.

## OS

### -Cofre
O objeto do cofre de serviços de recuperação correspondente ao cofre de serviços de recuperação.

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### Microsoft. Azure. Commands. Recoveryservices. ARSVault

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRVaultSettings

## INFORMA

## LINKS RELACIONADOS

