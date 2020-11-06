---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: 6591250c903b3f51ccbbd567e290f9d83fab983a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426860"
---
# Stop-AzureRmWebApp

## Sinopse
Interrompe um aplicativo Web do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Eles
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S2
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Stop-AzureRmWebApp** interrompe um aplicativo Web do Azure.

## EXEMPLOS

### Exemplo 1: parar um aplicativo Web
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

Esse comando interrompe o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.

## OS

### -Nome
Nome do WebApp

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Objeto WebApp

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
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

### Instalação
O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)

[New-AzureRmWebApp](./New-AzureRmWebApp.md)

[Remove-AzureRmWebApp](./Remove-AzureRmWebApp.md)

[Restart-AzureRmWebApp](./Restart-AzureRmWebApp.md)

[Start-AzureRmWebApp](./Start-AzureRmWebApp.md)


