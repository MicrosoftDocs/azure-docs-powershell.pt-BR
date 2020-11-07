---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 02291202966ab832bf11edbd59a1504c001c948e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770848"
---
# New-AzFrontDoorRoutingRuleObject

## Sinopse
Criar um PSRoutingRuleObject para a criação de porta frontal

## SYNTAX

### ByFieldsWithForwardingParameterSet
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFieldsWithRedirectParameterSet
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <PSRedirectType>] [-RedirectProtocol <PSRedirectProtocol>] [-CustomHost <String>]
 [-CustomPath <String>] [-CustomFragment <String>] [-CustomQueryString <String>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
Criar um PSRoutingRuleObject para a criação de porta frontal

## EXEMPLOS

### Exemplo 1: criar um PSRoutingRuleObject para a criação de porta frontal
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

Criar um PSRoutingRuleObject para a criação de porta frontal

## OS

### -AcceptedProtocol
Esquemas de protocolo para corresponder a essa regra.
O valor padrão é {https, http}

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPoolName
ID do recurso do BackendPool para o qual esta regra roteia

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomForwardingPath
O caminho personalizado usado para regravar caminhos de recursos correspondentes a essa regra.
Deixe em branco para usar o caminho de entrada.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomFragment
Fragmento para adicionar à URL de redirecionamento. Fragmento é a parte da URL que vem após #. Não inclua o #.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomHost
Host para redirecionar. Deixe em branco para usar o host de entrada como o host de destino.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomPath
O caminho completo para redirecionar. O caminho não pode estar vazio e deve começar com/. Deixe em branco para usar o caminho de entrada como caminho de destino.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomQueryString
O conjunto de cadeias de caracteres de consulta a serem colocadas na URL de redirecionamento. Definir esse valor substituiria qualquer cadeia de caracteres de consulta existente; Deixe em branco para preservar a cadeia de caracteres de consulta recebida. A cadeia de consulta deve estar em <key>=<value> Format. O primeiro? e & serão adicionados automaticamente para não incluí-los na frente, mas separe várias cadeias de caracteres de consulta com &.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DynamicCompression
Se a compactação dinâmica será habilitada para conteúdo em cache quando o armazenamento em cache estiver habilitado.
O valor padrão está habilitado

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCaching
Se o armazenamento em cache para esta rota deve ser habilitado. O valor padrão é falso

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enabledstate
Se o uso dessa regra deve ser habilitado.
O valor padrão está habilitado

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForwardingProtocol
O protocolo que essa regra usará ao encaminhar o tráfego para o valor padrão de back-ends é MatchRequest.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontDoorName
O nome da porta frontal à qual esta regra de roteamento pertence.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendEndpointName
Os nomes dos pontos de extremidade de front-end associados a essa regra

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do RoutingRule.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatternToMatch
Os padrões de rota da regra não devem ter *, exceto, após o final/no final do caminho. O valor padrão é/*

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryParameterStripDirective
O tratamento de termos de consulta de URL ao formar a chave de cache.
O valor padrão é StripAll

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectProtocol
O protocolo do destino para o qual o tráfego é redirecionado. O valor padrão é MatchRequest

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectProtocol
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Redirecttype
O tipo de redirecionamento que a regra usará ao redirecionar o tráfego. O valor padrão é movido

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectType
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: Moved, Found, TemporaryRedirect, PermanentRedirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos no qual o RoutingRule será criado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule

## INFORMA

## LINKS RELACIONADOS

[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)
