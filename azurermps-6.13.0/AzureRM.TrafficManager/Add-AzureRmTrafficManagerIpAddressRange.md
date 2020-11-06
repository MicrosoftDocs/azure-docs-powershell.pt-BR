---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427118"
---
# Add-AzureRmTrafficManagerIpAddressRange

## Sinopse
Adiciona uma sub-rede ou um intervalo de endereços a um objeto de ponto de extremidade do Gerenciador de tráfego local.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmTrafficManagerIpAddressRange** adiciona um intervalo de endereços IP a um objeto de ponto de extremidade do Azure Traffic Manager local.
Você pode obter um ponto de extremidade usando os cmdlets New-AzureRmTrafficManagerEndpoint ou Get-AzureRmTrafficManagerEndpoint.

Este cmdlet opera no objeto ponto de extremidade local.
Confirme as alterações no ponto de extremidade do Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerEndpoint.

## EXEMPLOS

### Exemplo 1: Adicionar intervalos de endereços IP a um ponto de extremidade
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

O primeiro comando cria um ponto de extremidade do Gerenciador de tráfego do Azure usando o cmdlet **New-AzureRmTrafficManagerEndpoint** .
O comando armazena o ponto de extremidade local na variável $TrafficManagerEndpoint.
O segundo comando adiciona o intervalo de endereços IP 1.2.3.4 a 5.6.7.8 ao ponto de extremidade armazenado em $TrafficManagerEndpoint.
O terceiro comando adiciona o intervalo de endereços IP 9.10.11.0 ao 9.10.11.255 ao ponto de extremidade armazenado em $TrafficManagerEndpoint.
O quarto comando verifica se o escopo corresponde ao tamanho do intervalo e, em seguida, adiciona o intervalo de endereços IP 12.13.14.0 ao 12.13.14.31 ao ponto de extremidade armazenado em $TrafficManagerEndpoint.
O quinto comando adiciona o intervalo de endereços IP 15.16.17.18 ao 15.16.17.18 ao ponto de extremidade armazenado em $TrafficManagerEndpoint.
O comando final atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.

## OS

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

### -Último
Especifica o último endereço IP no intervalo a ser adicionado.

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

### -Escopo
Especifica o escopo do intervalo de endereços IP a ser adicionado.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Especifica um objeto **TrafficManagerEndpoint** local.
Esse cmdlet modifica esse objeto local.
Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzureRmTrafficManagerEndpoint ou New-AzureRmTrafficManagerEndpoint.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Primeiro
Especifica o primeiro endereço IP do intervalo a ser adicionado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Este cmdlet aceita um objeto **TrafficManagerEndpoint** para este cmdlet.

## EXIBE

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Esse cmdlet retorna um objeto **TrafficManagerEndpoint** modificado.

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureRmTrafficManagerIpAddressRange](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
