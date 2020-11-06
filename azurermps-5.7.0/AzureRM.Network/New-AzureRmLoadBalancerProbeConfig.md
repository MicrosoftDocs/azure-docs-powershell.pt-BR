---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 0e5216f88cc860244cf11a693a73e30ba6e83390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432082"
---
# New-AzureRmLoadBalancerProbeConfig

## Sinopse
Cria uma configuração de sondagem para um balanceador de carga.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmLoadBalancerProbeConfig** cria uma configuração de teste para um balanceador de carga do Azure.

## EXEMPLOS

### Exemplo 1: criar uma configuração de sondagem
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

Esse comando cria uma configuração de sondagem chamada myprobe usando o protocolo HTTP.
O novo teste será conectado a um serviço de balanceamento de carga na porta 80.

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
Especifica o intervalo, em segundos, entre testes para cada instância de um serviço de balanceamento de carga.

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

### -Nome
Especifica o nome da configuração de sonda a ser criada.

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
Especifica a porta na qual o novo teste deve se conectar a um serviço de balanceamento de carga.

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
Especifica o protocolo a ser usado para a configuração de sondagem.
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
Especifica o caminho em um serviço de balanceamento de carga a ser sondado para determinar a integridade.

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

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSProbe

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmLoadBalancerProbeConfig](./Add-AzureRmLoadBalancerProbeConfig.md)

[Get-AzureRmLoadBalancerProbeConfig](./Get-AzureRmLoadBalancerProbeConfig.md)

[Remove-AzureRmLoadBalancerProbeConfig](./Remove-AzureRmLoadBalancerProbeConfig.md)

[Set-AzureRmLoadBalancerProbeConfig](./Set-AzureRmLoadBalancerProbeConfig.md)


