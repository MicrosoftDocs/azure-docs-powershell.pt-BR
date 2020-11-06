---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 5655272afa9ddc9c0ff4c1873a0fac7a0e1f50dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427844"
---
# Remove-AzureRmApplicationGatewayBackendAddressPool

## Sinopse
Remove um pool de endereços back-end de um gateway de aplicativo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmApplicationGatewayBackendAddressPool** remove um pool de endereços back-end de um gateway do aplicativo do Azure.

## EXEMPLOS

### Exemplo 1: remover um pool de endereços back-end de um aplicativo gateway
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

O primeiro comando obtém o gateway do aplicativo denominado ApplicationGateway01 pertencente ao grupo de recursos chamado ResourceGroup01 e salva-o na variável $AppGw.

O segundo comando Remove o pool de endereços back-end chamado BackEndPool02 do gateway do aplicativo.

## OS

### -ApplicationGateway
Especifica o Application Gateway do qual esse cmdlet Remove um pool de endereços back-end.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do pool de endereços back-end que este cmdlet Remove.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

### System. String

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmApplicationGatewayBackendAddressPool](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[Get-AzureRmApplicationGatewayBackendAddressPool](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[New-AzureRmApplicationGatewayBackendAddressPool](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[Set-AzureRmApplicationGatewayBackendAddressPool](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


