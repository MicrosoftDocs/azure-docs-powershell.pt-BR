---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945664"
---
# Get-AzureApplicationGatewaySslCertificate

## Sinopse
Obtém certificados de gateway de aplicativo.

## SYNTAX

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureApplicationGatewaySslCertificate** obtém certificados SSL (Secure Sockets Layer) para um gateway do aplicativo do Azure.

## EXEMPLOS

### Exemplo 1: obter um certificado SSL
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

Esse comando obtém um certificado SSL chamado SslCertificate13 no gateway do aplicativo chamado ApplicationGateway08.

### Exemplo 2: obter todos os certificados SSL
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

Esse comando obtém todos os certificados SSL no gateway do aplicativo chamado ApplicationGateway08.

## OS

### -CertificateName
Especifica o nome de um certificado SSL.
Esse cmdlet obtém o certificado que esse parâmetro especifica.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do aplicativo do gateway do qual esse cmdlet obtém um certificado SSL.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
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

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, List<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate>

## INFORMA

## LINKS RELACIONADOS

[Add-AzureApplicationGatewaySslCertificate](./Add-AzureApplicationGatewaySslCertificate.md)

[Remove-AzureApplicationGatewaySslCertificate](./Remove-AzureApplicationGatewaySslCertificate.md)
