---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 1cb180d96b99a7dc2286c45a1d3f81a03a9cb212
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786498"
---
# Add-AzureRmRouteFilterRuleConfig

## Sinopse
Adiciona uma regra de filtro de rota a um filtro de rota.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Add-AzureRmRouteFilterRuleConfig adiciona uma regra de filtro de rota a um filtro de rota do Azure.

## EXEMPLOS

### --------------------------Exemplo 1: adicionar uma regra de filtro de rota a um filtro de rota--------------------------
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

O primeiro comando obtém um filtro de rota chamado routefilter01 usando o cmdlet Get-AzureRmRouteFilter.
O comando armazena o filtro na variável $RouteFilter.

## OS

### -Acesso
Especifica o acesso da regra de filtro de rota, os valores válidos são Deny ou Allow.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Communitylist
A lista de valor da Comunidade para a qual o filtro de rota será filtrado

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Force
Não pedir confirmação se quiser sobreformular um recurso

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

### -Nome
Especifica um nome da regra de filtro de rota a ser adicionada ao filtro de rota.

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

### -RouteFilter
Especifica o filtro de rota para o qual esse cmdlet adiciona uma regra de filtro de rota.

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RouteFilterRuleType
Especifica o tipo de regra do filtro de rota.
Os valores válidos são: Comunidade

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### PSRouteFilter
O parâmetro ' RouteFilter ' aceita o valor do tipo ' PSRouteFilter ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSRouteFilter

## INFORMA
Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede

## LINKS RELACIONADOS

[Get-AzureRmRouteFilterRuleConfig](./Get-AzureRmRouteFilterRuleConfig.md)

[Get-AzureRmRouteFilter](./Get-AzureRmRouteFilter.md)







[Set-AzureRmRouteFilter](./Set-AzureRmRouteFilter.md)

