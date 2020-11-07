---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9e15979b7e54ef926e7b4355a70568f39594112f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772768"
---
# New-AzTrafficManagerEndpoint

## Sinopse
Cria um ponto de extremidade em um perfil do Gerenciador de tráfego.

## SYNTAX

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzTrafficManagerEndpoint** cria um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.

Esse cmdlet confirma cada novo ponto de extremidade para o serviço do Gerenciador de tráfego.
Para adicionar vários pontos de extremidade a um objeto de perfil do Gerenciador de tráfego local e confirmar as alterações em uma única operação, use o cmdlet Add-AzTrafficManagerEndpointConfig.

## EXEMPLOS

### Exemplo 1: criar um ponto de extremidade externo para um perfil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Esse comando cria um ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11.

### Exemplo 2: criar um ponto de extremidade do Azure para um perfil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Esse comando cria um ponto de extremidade do Azure chamado contoso no perfil chamado ContosoProfile na ResourceGroup11 do grupo de recursos.
O ponto de extremidade do Azure aponta para o aplicativo Web do Azure cuja ID do Gerenciador de recursos do Azure é fornecida pelo caminho de URI no *TargetResourceId*.
O comando não especifica o parâmetro *EndpointLocation* porque o recurso do aplicativo Web fornece o local.

## OS

### -CustomHeader
Lista de pares de nome e valor do cabeçalho personalizado para solicitações de sondagem.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
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

### -EndpointLocation
Especifica o local do ponto de extremidade a ser usado no método de roteamento de tráfego de desempenho.
Esse parâmetro é aplicável somente a pontos de extremidade do tipo ExternalEndpoints ou NestedEndpoints.
Você deve especificar esse parâmetro quando o método de roteamento de tráfego de desempenho for usado.

Especifique um nome de região do Azure.
Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

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

### -EndpointStatus
Especifica o status do ponto de extremidade.
Os valores válidos são: 

- Possibilita 
- Ativo 

Se o status estiver habilitado, o ponto de extremidade será analisado para a integridade do ponto de extremidade e será incluído no método de roteamento de tráfego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geomapping
A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego ' geográfico '. Consulte a documentação do Gerenciador de tráfego para obter uma lista completa de valores aceitos.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Especifique um nome de região do Azure.
Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do ponto de extremidade do Gerenciador de tráfego que este cmdlet cria.

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

### -Priority
Especifica a prioridade que o Gerenciador de tráfego atribui ao ponto de extremidade.
Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método para roteamento de tráfego prioritário.
Os valores válidos são inteiros de 1 a 1000.
Valores inferiores representam prioridade mais alta.

Se você especificar uma prioridade, deverá especificar prioridades em todos os pontos de extremidade do perfil, e nenhum dois pontos de extremidade poderá compartilhar o mesmo valor de prioridade.
Se você não especificar prioridades, o Gerenciador de tráfego atribuirá valores de prioridade padrão aos pontos de extremidade, começando com um (1), na ordem em que o perfil lista os pontos de extremidade.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
Especifica o nome de um perfil do Gerenciador de tráfego ao qual esse cmdlet adiciona um ponto de extremidade.
Para obter um perfil, use os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile.

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

### -ResourceGroupName
Especifica o nome de um grupo de recursos.
Esse cmdlet cria um ponto de extremidade do Gerenciador de tráfego no grupo que esse parâmetro especifica.

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

### -SubnetMapping
A lista de intervalos de endereços ou sub-redes mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego "sub-rede".

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destino
Especifica o nome DNS totalmente qualificado do ponto de extremidade.
O Gerenciador de tráfego retorna esse valor em respostas DNS quando direciona o tráfego para esse ponto de extremidade.
Especifique esse parâmetro somente para o tipo de ponto de extremidade ExternalEndpoints.
Para outros tipos de ponto de extremidade, especifique o parâmetro *TargetResourceId* em vez disso.

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

### -TargetResourceId
Especifica a ID do recurso do destino.
Especifique esse parâmetro somente para os tipos de ponto de extremidade AzureEndpoints e NestedEndpoints.
Para o tipo de ponto de extremidade ExternalEndpoints, especifique o parâmetro de *destino* em vez disso.

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

### -Digite
Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.
Os valores válidos são: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Weight
Especifica a espessura que o Gerenciador de tráfego atribui ao ponto de extremidade.
Os valores válidos são inteiros de 1 a 1000.
O valor padrão é um (1).
Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método de direcionamento de tráfego ponderado.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

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

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint

## INFORMA

## LINKS RELACIONADOS

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


