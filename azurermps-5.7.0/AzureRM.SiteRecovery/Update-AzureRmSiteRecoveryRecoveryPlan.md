---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 594cb9af7c1afb82187003e3ddd7c085a254c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426584"
---
# Update-AzureRmSiteRecoveryRecoveryPlan

## Sinopse
Atualiza um plano de recuperação na recuperação do site.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByRPObject (padrão)
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRPFile
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzureRmSiteRecoveryRecoveryPlan** atualiza um plano de recuperação no Azure site Recovery e, em seguida, o publica.

## EXEMPLOS

### Exemplo 1: atualizar um plano de recuperação
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

Esse comando atualiza o plano de recuperação especificado e o publica.

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

### -Caminho
Especifica o caminho do arquivo de plano de recuperação do plano de recuperação que este cmdlet atualiza.

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Especifica um plano de recuperação que este cmdlet atualiza.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
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

### ASRRecoveryPlan
O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSiteRecoveryRecoveryPlan](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[New-AzureRmSiteRecoveryRecoveryPlan](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[Remove-AzureRmSiteRecoveryRecoveryPlan](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


