---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 147727cffc03de5ba8848705cf79facdbdc43320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430180"
---
# Get-AzureRmApplicationGatewayConnectionDraining

## Sinopse
Obtém a conexão que descarrega a configuração de um objeto de configurações HTTP back-end.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApplicationGatewayConnectionDraining** Obtém a configuração de descarga da configuração de um objeto de configurações http back-end.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.
O segundo comando obtém as configurações HTTP back-end chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.
O último comando obtém a conexão que descarrega a configuração das configurações HTTP back-end $Settings e a armazena na variável $ConnectionDraining.

## OS

### -BackendHttpSettings
As configurações http de back-end

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings
Parâmetros: BackendHttpSettings (ByValue)

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[Get-AzureRmApplicationGatewayBackendHttpSettings](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[New-AzureRmApplicationGatewayConnectionDraining](./New-AzureRmApplicationGatewayConnectionDraining.md)

[Remove-AzureRmApplicationGatewayConnectionDraining](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[Set-AzureRmApplicationGatewayConnectionDraining](./Set-AzureRmApplicationGatewayConnectionDraining.md)
