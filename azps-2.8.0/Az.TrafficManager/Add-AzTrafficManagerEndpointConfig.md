---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 0ad478b1e60008619e579abf868f4d6aba25bbd9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773142"
---
# Add-AzTrafficManagerEndpointConfig

## Sinopse
Adiciona um ponto de extremidade a um objeto de perfil do Gerenciador de tráfego local.

## SYNTAX

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzTrafficManagerEndpointConfig** adiciona um ponto de extremidade a um objeto de perfil do Azure Traffic Manager local.
Você pode obter um perfil usando os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile.

Este cmdlet opera no objeto de perfil local.
Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzTrafficManagerProfile.
Para criar um ponto de extremidade e confirmar a alteração em uma única operação, use o cmdlet New-AzTrafficManagerEndpoint.

## EXEMPLOS

### Exemplo 1: adicionar um ponto de extremidade a um perfil
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile** .
O comando armazena o perfil local na variável $TrafficManagerProfile.

O segundo comando adiciona um ponto de extremidade chamado contoso ao perfil armazenado em $TrafficManagerProfile.
O comando inclui dados de configuração para o ponto de extremidade.
Esse comando altera somente o objeto local.

O comando final atualiza o perfil do Gerenciador de tráfego no Azure para corresponder ao valor local em $TrafficManagerProfile.

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

### -EndpointName
Especifica o nome do ponto de extremidade do Gerenciador de tráfego que o cmdlet adiciona.

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
A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego ' geográfico '. Consulte a documentação do Gerenciador de tráfego para obter uma [lista completa de valores aceitos](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).

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
O número mínimo de pontos de extremidade que devem estar disponíveis no perfil filho para que o ponto de extremidade aninhado no perfil pai seja considerado disponível.
Aplicável somente ao ponto de extremidade do tipo ' NestedEndpoints '.

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

### -TrafficManagerProfile
Especifica um objeto **TrafficManagerProfile** local.
Esse cmdlet modifica esse objeto local.
Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzTrafficManagerProfile.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego do Azure.
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

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile

## EXIBE

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile

## INFORMA

## LINKS RELACIONADOS

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


