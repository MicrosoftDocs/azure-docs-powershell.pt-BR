---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 5657701475e81b302d761193cd542ee38ea9c16e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430616"
---
# Remove-AzureRmSiteRecoveryRecoveryPlan

## Sinopse
Remove um plano de recuperação de site da recuperação do site.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByObject (padrão)
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmSiteRecoveryRecoveryPlan** remove um plano de recuperação de site do Azure site Recovery atual.

## EXEMPLOS

### Exemplo 1: remover um plano de recuperação
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

O primeiro comando usa o cmdlet Get-AzureRmSiteRecoveryRecoveryPlan para obter o plano de recuperação do site e, em seguida, armazena-o na variável $RecoveryPlan.

O segundo comando Remove o plano de recuperação em $RecoveryPlan.

## OS

### -Nome
Especifica o nome do plano de recuperação que este cmdlet Remove.

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

### -RecoveryPlan
Especifica o plano de recuperação que este cmdlet Remove.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### ASRRecoveryPlan
O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSiteRecoveryRecoveryPlan](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[New-AzureRmSiteRecoveryRecoveryPlan](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[Update-AzureRmSiteRecoveryRecoveryPlan](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


