---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: f0d537e2729fc69f2a65563ab059f332d320e99a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431108"
---
# Get-AzureRmRouteConfig

## Sinopse
Obtém rotas de uma tabela de rota.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmRouteConfig [-Name <String>] -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmRouteConfig** Obtém rotas de uma tabela de rota do Azure.
Você pode especificar uma rota por nome.

## EXEMPLOS

### Exemplo 1: obter uma tabela de rota
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet **Get-AzureRmRouteTable** .
O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.
O cmdlet atual Obtém a rota chamada Route07 na tabela de rota chamada RouteTable01.

## OS

### -Nome
Especifica o nome da rota obtida por esse cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RouteTable
Especifica a tabela de rotas da qual esse cmdlet obtém rotas.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
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

### PSRouteTable
O parâmetro ' RouteTable ' aceita o valor do tipo ' PSRouteTable ' da pipeline

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSRoute

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmRouteConfig](./Add-AzureRmRouteConfig.md)

[Get-AzureRmRouteTable](./Get-AzureRmRouteTable.md)

[New-AzureRmRouteConfig](./New-AzureRmRouteConfig.md)

[Remove-AzureRmRouteConfig](./Remove-AzureRmRouteConfig.md)

[Set-AzureRmRouteConfig](./Set-AzureRmRouteConfig.md)


