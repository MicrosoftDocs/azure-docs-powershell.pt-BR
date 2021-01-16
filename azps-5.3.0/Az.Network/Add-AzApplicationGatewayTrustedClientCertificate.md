---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271894"
---
# Add-AzApplicationGatewayTrustedClientCertificate

## Sinopse
Adiciona uma cadeia de certificados de autoridade de certificação de cliente confiável a um gateway de aplicativo.

## SYNTAX

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzApplicationGatewayTrustedClientCertificate** adiciona uma cadeia de certificados de autoridade de certificação de cliente confiável a um aplicativo gateway do Azure.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável. O segundo comando cria uma nova cadeia de certificados de autoridade de certificação de cliente confiável fazendo o caminho do certificado de CA do cliente como entrada. O terceiro comando cria um perfil SSL usando um certificado de cliente confiável. O quarto comando atualiza o Application Gateway.

## OS

### -ApplicationGateway
O applicationGateway

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

### -CertificateFile
Caminho do arquivo de cadeia de certificados da autoridade de certificação do cliente confiável

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome da cadeia de certificados da autoridade de certificação do cliente confiável

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## INFORMA

## LINKS RELACIONADOS

[New-AzApplicationGatewayTrustedClientCertificate](./New-AzApplicationGatewayTrustedClientCertificate.md)

[Get-AzApplicationGatewayTrustedClientCertificate](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[Remove-AzApplicationGatewayTrustedClientCertificate](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[Set-AzApplicationGatewayTrustedClientCertificate](./Set-AzApplicationGatewayTrustedClientCertificate.md)