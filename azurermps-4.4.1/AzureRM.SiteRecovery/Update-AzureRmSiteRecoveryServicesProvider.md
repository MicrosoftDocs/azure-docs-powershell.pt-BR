---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 31eda861294d4c678e141da8f40d1f5d6c5a4ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609555"
---
# Update-AzureRmSiteRecoveryServicesProvider

## Sinopse
Atualiza as informações recebidas do provedor de serviços de recuperação de site do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzureRmSiteRecoveryServicesProvider** atualiza as informações recebidas do provedor de serviços de recuperação de site do Azure.
Você pode usar esse cmdlet para disparar uma atualização das informações recebidas do provedor de serviços de recuperação.

## EXEMPLOS

## OS

### -Servicesprovider
Especifica o objeto do provedor de serviços de recuperação do site do Azure.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
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

### ASRRecoveryServicesProvider
O parâmetro ' Servicesprovider ' aceita o valor do tipo ' ASRRecoveryServicesProvider ' da pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSiteRecoveryServicesProvider](./Get-AzureRmSiteRecoveryServicesProvider.md)

[Remove-AzureRmSiteRecoveryServicesProvider](./Remove-AzureRmSiteRecoveryServicesProvider.md)
