---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 38a7f8ee32f02db10dc971d5be2016d5dea0b538
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426605"
---
# New-AzureRmSiteRecoveryFabric

## Sinopse
Cria uma malha do Azure site Recovery.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmSiteRecoveryFabric** cria uma malha de recuperação de site do Azure do tipo especificado.

## EXEMPLOS

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
Especifica o nome da malha de recuperação do site do Azure

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de malha do Azure site Recovery.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. SiteRecovery. ASRJob

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSiteRecoveryFabric](./Get-AzureRmSiteRecoveryFabric.md)

[Remove-AzureRmSiteRecoveryFabric](./Remove-AzureRmSiteRecoveryFabric.md)
