---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bec9d197d039ea3934607ee291bdd6511ae6f4a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432090"
---
# Get-AzureRmApplicationGatewayAuthenticationCertificate

## Sinopse
Obtém um certificado de autenticação para um gateway de aplicativo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApplicationGatewayAuthenticationCertificate** Obtém um certificado de autenticação para um gateway do aplicativo do Azure.

## EXEMPLOS

## OS

### -ApplicationGateway
Especifica o nome do gateway do aplicativo para o qual esse cmdlet obtém um certificado de autenticação.

```yaml
Type: PSApplicationGateway
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do certificado de autenticação que este cmdlet obtém.

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

### System. String

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate

## INFORMA
* Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede

## LINKS RELACIONADOS

[Add-AzureRmApplicationGatewayAuthenticationCertificate](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[New-AzureRmApplicationGatewayAuthenticationCertificate](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[Remove-AzureRmApplicationGatewayAuthenticationCertificate](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[Set-AzureRmApplicationGatewayAuthenticationCertificate](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


