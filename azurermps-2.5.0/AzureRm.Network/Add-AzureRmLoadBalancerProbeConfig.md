---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: a6fe4515fe6e6df213abb667eb83bccfa9ac6095
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786500"
---
# Add-AzureRmLoadBalancerProbeConfig

## Sinopse
Adiciona uma configuração de teste a um balanceador de carga.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmLoadBalancerProbeConfig** adiciona uma configuração de teste a um balanceador de carga do Azure.

## EXEMPLOS

### Exemplo 1 adicionar uma configuração de teste a um balanceador de carga
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

Esse comando obtém o balanceador de carga chamado myLb, adiciona a configuração de teste especificada a ele e, em seguida, usa o cmdlet **set-AzureRmLoadBalancer** para atualizar o balanceador de carga.

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

### -IntervalInSeconds
Especifica o intervalo, em segundos, entre testes para cada instância do serviço de balanceamento de carga.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Loadbalancer
Especifica um objeto **Loadbalancer** .
Esse cmdlet adiciona uma configuração de teste ao balanceador de carga que o parâmetro especifica.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da configuração de sonda a ser adicionada.

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

### -Porta
Especifica a porta na qual os testes devem se conectar a um serviço de balanceamento de carga.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeCount
Especifica o número de falhas consecutivas por instância para que uma instância seja considerada não íntegra.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocolo
Especifica o protocolo a ser usado para o teste.
Os valores aceitáveis para esse parâmetro são: TCP ou http.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestPath
Especifica o caminho no serviço de balanceamento de carga a ser sondado para determinar a integridade.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSLoadBalancer
O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmLoadBalancerProbeConfig](./Get-AzureRmLoadBalancerProbeConfig.md)

[New-AzureRmLoadBalancerProbeConfig](./New-AzureRmLoadBalancerProbeConfig.md)

[Remove-AzureRmLoadBalancerProbeConfig](./Remove-AzureRmLoadBalancerProbeConfig.md)

[Set-AzureRmLoadBalancer](./Set-AzureRmLoadBalancer.md)

[Set-AzureRmLoadBalancerProbeConfig](./Set-AzureRmLoadBalancerProbeConfig.md)


