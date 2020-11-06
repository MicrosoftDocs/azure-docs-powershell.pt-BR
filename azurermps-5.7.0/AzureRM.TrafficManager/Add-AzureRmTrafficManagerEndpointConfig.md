---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: e9e6817d9a290acf1e91067edfd90cdf8081f1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432375"
---
# Add-AzureRmTrafficManagerEndpointConfig

## Sinopse
Adiciona um ponto de extremidade a um objeto de perfil do Gerenciador de tráfego local.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmTrafficManagerEndpointConfig** adiciona um ponto de extremidade a um objeto de perfil do Azure Traffic Manager local.
Você pode obter um perfil usando os cmdlets New-AzureRmTrafficManagerProfile ou Get-AzureRmTrafficManagerProfile.

Este cmdlet opera no objeto de perfil local.
Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerProfile.
Para criar um ponto de extremidade e confirmar a alteração em uma única operação, use o cmdlet New-AzureRmTrafficManagerEndpoint.

## EXEMPLOS

### Exemplo 1: adicionar um ponto de extremidade a um perfil
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzureRmTrafficManagerProfile** .
O comando armazena o perfil local na variável $TrafficManagerProfile.

O segundo comando adiciona um ponto de extremidade chamado contoso ao perfil armazenado em $TrafficManagerProfile.
O comando inclui dados de configuração para o ponto de extremidade.
Esse comando altera somente o objeto local.

O comando final atualiza o perfil do Gerenciador de tráfego no Azure para corresponder ao valor local em $TrafficManagerProfile.

## OS

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

### -EndpointLocation
Especifica o local do ponto de extremidade a ser usado no método de roteamento de tráfego de desempenho.
Esse parâmetro é aplicável somente a pontos de extremidade do tipo ExternalEndpoints ou NestedEndpoints.
Você deve especificar esse parâmetro quando o método de roteamento de tráfego de desempenho for usado.

Especifique um nome de região do Azure.
Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

```yaml
Type: String
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
Type: String
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
Type: String
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
Especifique um nome de região do Azure.
Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

```yaml
Type: UInt32
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
Type: UInt32
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
Type: String
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
Type: String
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
Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.

```yaml
Type: TrafficManagerProfile
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
Type: String
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
Type: UInt32
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

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Este cmdlet aceita um objeto **TrafficManagerProfile** para este cmdlet.

## EXIBE

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Esse cmdlet retorna um objeto **TrafficManagerProfile** modificado.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


