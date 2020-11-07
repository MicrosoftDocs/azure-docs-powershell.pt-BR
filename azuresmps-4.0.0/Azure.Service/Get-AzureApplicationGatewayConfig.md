---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945665"
---
# Get-AzureApplicationGatewayConfig

## Sinopse
Obtém um contexto de configuração de gateway de aplicativo.

## SYNTAX

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureApplicationGatewayConfig** Obtém um contexto de configuração do Azure Application Gateway.
Um contexto inclui um objeto de configuração e uma configuração XML.
Você pode salvar a configuração XML em um arquivo.

## EXEMPLOS

### Exemplo 1: obter uma configuração de gateway de aplicativo e salvá-la em um arquivo
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

Esse comando obtém a configuração de um gateway de aplicativo chamado ApplicationGateway06.
O comando salva-o no arquivo no caminho especificado.

## OS

### -ExportToFile
Especifica um caminho de arquivo para o qual esse cmdlet salva a configuração no formato XML.

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

### -Nome
Especifica o nome do gateway do aplicativo para o qual este cmdlet obtém informações de configuração.

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
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

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

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext

## INFORMA

## LINKS RELACIONADOS

[Set-AzureApplicationGatewayConfig](./Set-AzureApplicationGatewayConfig.md)


