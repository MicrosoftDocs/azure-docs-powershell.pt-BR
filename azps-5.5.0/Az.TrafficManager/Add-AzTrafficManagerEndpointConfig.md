---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118513"
---
# Add-AzTrafficManagerEndpointConfig

## Sinopse
Adiciona um ponto de extremidade a um objeto de perfil local do Gerenciador de Tráfego.

## Sintaxe

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O **cmdlet Add-AzTrafficManagerEndpointConfig** adiciona um ponto de extremidade a um objeto de perfil local do Gerenciador de Tráfego do Azure.
Você pode obter um perfil usando os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile dados.

Este cmdlet opera no objeto de perfil local.
Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.
Para criar um ponto de extremidade e comprometer a alteração em uma única operação, use New-AzTrafficManagerEndpoint cmdlet.

## Exemplos

### Exemplo 1: Adicionar um ponto de extremidade a um perfil
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile.**
O comando armazena o perfil local na variável $TrafficManagerProfile dados.

O segundo comando adiciona um ponto de extremidade chamado contoso ao perfil armazenado $TrafficManagerProfile.
O comando inclui dados de configuração para o ponto de extremidade.
Esse comando altera apenas o objeto local.

O comando final atualiza o perfil do Gerenciador de Tráfego no Azure para corresponder ao valor local no $TrafficManagerProfile.

## Parâmetros

### -CustomHeader
Lista de nomes de cabeça personalizados e pares de valores para solicitações de solicitação de confirmação.

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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
Este parâmetro só é aplicável aos pontos de extremidade dos Pontos Externos ou do tipo AninhadoEndpoints.
Você deve especificar esse parâmetro quando o método de roteamento de tráfego de desempenho for usado.

Especifique um nome de região do Azure.
Para ver uma lista completa de regiões do Azure, consulte Regiões do Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

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

### -Nomedo Ponto de Extremidade
Especifica o nome do ponto de extremidade do Gerenciador de Tráfego que este cmdlet adiciona.

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

- Habilitado 
- Desativado 

Se o status estiver habilitado, o ponto de extremidade será substituído pela saúde do ponto de extremidade e será incluído no método de roteamento de tráfego.

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

### -GeoMapping
A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego "Geográfico". Consulte a documentação do Gerenciador de Tráfego para ver uma [lista completa de valores aceitos.](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)

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
O número mínimo de pontos de extremidade que devem estar disponíveis no perfil filho para que o Ponto de Extremidade Aninhado no perfil pai seja considerado disponível.
Aplicável somente ao ponto de extremidade do tipo "Aninhados".

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

### -Prioridade
Especifica a prioridade que o Gerenciador de Tráfego atribui ao ponto de extremidade.
Esse parâmetro será usado somente se o perfil do Gerenciador de Tráfego estiver configurado com o método de roteamento de tráfego de prioridade.
Os valores válidos são números inteiros de 1 a 1000.
Valores inferiores representam prioridade mais alta.

Se você especificar uma prioridade, deverá especificar prioridades em todos os pontos de extremidade no perfil e nenhum dois pontos de extremidade poderá compartilhar o mesmo valor de prioridade.
Se você não especificar prioridades, o Gerenciador de Tráfego atribuirá valores de prioridade padrão aos pontos de extremidade, começando com um (1), na ordem em que o perfil lista os pontos de extremidade.

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

### -Sub-RedeMapping
A lista de intervalos de endereços ou sub-redes mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego "Sub-rede".

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
O Gerenciador de Tráfego retorna esse valor em respostas DNS quando direciona o tráfego para esse ponto de extremidade.
Especifique esse parâmetro somente para o tipo de ponto de extremidade ExternalEndpoints.
Para outros tipos de ponto de extremidade, especifique o parâmetro *TargetResourceId.*

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
Especifica a ID de recurso do destino.
Especifique esse parâmetro somente para os tipos de pontos de extremidade AzureEndpoints e Aninhados.
Para o tipo de ponto de extremidade ExternalEndpoints, especifique o *parâmetro* Destino.

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
Este cmdlet modifica este objeto local.
Para obter um **objeto TrafficManagerProfile,** use o cmdlet Get-AzTrafficManagerProfile dados.

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

### -Tipo
Especifica o tipo de ponto de extremidade que esse cmdlet adiciona ao perfil do Gerenciador de Tráfego do Azure.
Os valores válidos são: 

- Pontos do AzureEnd
- Pontos Externos
- Pontos aninhados

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

### -Peso
Especifica a peso que o Gerenciador de Tráfego atribui ao ponto de extremidade.
Os valores válidos são números inteiros de 1 a 1000.
O valor padrão é um (1).
Esse parâmetro será usado somente se o perfil do Gerenciador de Tráfego estiver configurado com o método de roteamento de tráfego ponderado.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## Saídas

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## Notas

## LINKS RELACIONADOS

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


