---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115595"
---
# New-AzTrafficManagerEndpoint

## Sinopse
Cria um ponto de extremidade em um perfil do Gerenciador de Tráfego.

## Sintaxe

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **New-AzTrafficManagerEndpoint** cria um ponto de extremidade em um perfil do Gerenciador de Tráfego do Azure.

Este cmdlet confirma cada novo ponto de extremidade para o serviço gerenciador de tráfego.
Para adicionar vários pontos de extremidade a um objeto de perfil local do Gerenciador de Tráfego e comprometer as alterações em uma única operação, use o cmdlet Add-AzTrafficManagerEndpointConfig controle.

## Exemplos

### Exemplo 1: Criar um ponto de extremidade externo para um perfil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Esse comando cria um ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11.

### Exemplo 2: Criar um ponto de extremidade do Azure para um perfil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Esse comando cria um ponto de extremidade do Azure chamado contoso no perfil chamado ContosoProfile no grupo de recursos ResourceGroup11.
O ponto de extremidade do Azure aponta para o Azure Web App cuja ID do Gerenciador de Recursos do Azure é dada pelo caminho do URI no *TargetResourceId.*
O comando não especifica o parâmetro *EndpointLocation* porque o recurso do Web App fornece o local.

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
Este parâmetro só é aplicável aos pontos de extremidade do tipo ExternalEndpoints ou Aninhados.
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
A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego "Geográfico". Consulte a documentação do Gerenciador de Tráfego para ver uma lista completa de valores aceitos.

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
Para ver uma lista completa de regiões do Azure, consulte Regiões do Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

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
Especifica o nome do ponto de extremidade do Gerenciador de Tráfego que este cmdlet cria.

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

### -ProfileName
Especifica o nome de um perfil do Gerenciador de Tráfego ao qual este cmdlet adiciona um ponto de extremidade.
Para obter um perfil, use os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile dados.

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
Esse cmdlet cria um ponto de extremidade do Gerenciador de Tráfego no grupo especificado por esse parâmetro.

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

### -Tipo
Especifica o tipo de ponto de extremidade que esse cmdlet adiciona ao perfil do Gerenciador de Tráfego.
Os valores válidos são: 

- Pontos do AzureEnd
- Pontos Externos
- Pontos Aninhados

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

### Nenhum

## Saídas

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## Notas

## LINKS RELACIONADOS

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


