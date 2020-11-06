---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427101"
---
# Remove-AzureRmTrafficManagerIpAddressRange

## Sinopse
Remove uma sub-rede ou um intervalo de endereços de um objeto de ponto de extremidade do Gerenciador de tráfego local.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmTrafficManagerIpAddressRange** remove um intervalo de endereços IP de um objeto de ponto de extremidade do Azure Traffic Manager local.
Você pode obter um ponto de extremidade usando os cmdlets New-AzureRmTrafficManagerEndpoint ou Get-AzureRmTrafficManagerEndpoint.

Este cmdlet opera no objeto ponto de extremidade local.
Confirme as alterações no ponto de extremidade do Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerEndpoint.

## EXEMPLOS

### Exemplo 1: remover intervalos de endereços IP de um ponto de extremidade
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

O primeiro comando obtém o ponto de extremidade do Azure chamado contoso do perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $TrafficManagerEndpoint.
O segundo comando Remove um intervalo de endereços IP do ponto de extremidade armazenado no $TrafficManagerEndpoint.
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
Especifica o primeiro endereço IP do intervalo a ser removido.

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
Esse cmdlet retorna um objeto TrafficManagerEndpoint modificado.

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmTrafficManagerIpAddressRange](./Add-AzureRmTrafficManagerIpAddressRange.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
