---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598388"
---
# Remove-AzTrafficManagerEndpointConfig

## Sinopse
Remove um ponto de extremidade de um objeto de perfil do Gerenciador de tráfego local.

## SYNTAX

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzTrafficManagerEndpointConfig** remove um ponto de extremidade de um objeto de perfil do Gerenciador de tráfego do Azure local.
Você pode obter um perfil usando o cmdlet Get-AzTrafficManagerProfile.

Este cmdlet opera no objeto de perfil local.
Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzTrafficManagerProfile.
Para remover um ponto de extremidade e confirmar as alterações em uma única operação, use o cmdlet Remove-AzTrafficManagerEndpoint.

## EXEMPLOS

### Exemplo 1: remover um ponto de extremidade
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile** .
O comando armazena o perfil local na variável $TrafficManagerProfile.

O segundo comando Remove um ponto de extremidade do Azure chamado contoso do perfil armazenado em $TrafficManagerProfile.
Esse comando altera somente o objeto local.

O comando final atualiza o perfil do Gerenciador de tráfego chamado ContosoProfile para corresponder ao valor local em $TrafficManagerProfile.

## OS

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

### -EndpointName
Especifica o nome do ponto de extremidade do Gerenciador de tráfego que este cmdlet Remove.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile

## EXIBE

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile

## INFORMA

## LINKS RELACIONADOS

[Add-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


