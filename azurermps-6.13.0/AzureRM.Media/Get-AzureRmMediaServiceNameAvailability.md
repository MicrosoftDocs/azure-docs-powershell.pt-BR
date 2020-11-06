---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: 8de8b9f389f8d57d844c17d92dd492390fbf1884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428087"
---
# Get-AzureRmMediaServiceNameAvailability

## Sinopse
Verifica se um nome de serviço de mídia está disponível.
Os nomes de serviços de mídia são exclusivos globalmente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmMediaServiceNameAvailability** verifica se um nome de serviço de mídia está disponível.
Os nomes de serviços de mídia são exclusivos globalmente.

## EXEMPLOS

### Exemplo 1: verificar se um nome de serviço de mídia está disponível
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

Esse comando verifica se o nome MediaService1 está disponível.

## OS

### -AccountName
Especifica o nome do serviço de mídia que este cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmMediaService](./Get-AzureRmMediaService.md)

[New-AzureRmMediaService](./New-AzureRmMediaService.md)

[Remove-AzureRmMediaService](./Remove-AzureRmMediaService.md)

[Set-AzureRmMediaService](./Set-AzureRmMediaService.md)


