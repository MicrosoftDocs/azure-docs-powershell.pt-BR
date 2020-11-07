---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946429"
---
# Set-AzureApplicationGatewayConfig

## Sinopse
Configura um gateway de aplicativo.

## SYNTAX

### ConfigFile
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configobject
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureApplicationGatewayConfig** configura um gateway de aplicativo.

## EXEMPLOS

### Exemplo 1: configurar um gateway de aplicativo usando um objeto de configuração
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

O primeiro comando obtém o objeto de configuração para o gateway do aplicativo chamado ApplicationGateway02 usando o cmdlet **Get-AzureApplicationGatewayConfig** .
O comando o armazena na variável $ConfigReturnObject.

O segundo comando define a configuração do aplicativo chamado ApplicationGateway06 usando um objeto de configuração do Application Gateway armazenado na variável $ConfigReturnObject.

### Exemplo 2: configurar um gateway de aplicativo usando um arquivo de configuração
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

Esse comando define a configuração do aplicativo chamado ApplicationGateway06 usando um arquivo de configuração de gateway do aplicativo no local especificado.

### Exemplo 3: modificar uma configuração usando um objeto de configuração
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

O primeiro comando obtém o objeto de configuração para o gateway do aplicativo chamado ApplicationGateway06 usando o cmdlet **Get-AzureApplicationGatewayConfig** .
O comando o armazena na variável $ConfigReturnObject.

O segundo comando atribui um valor de porta a uma propriedade de **porta** no objeto armazenado em $ConfigReturnObject.

O comando final passa o $ConfigReturnObject atualizado para o cmdlet atual.

## OS

### -Config
Especifica um objeto de configuração de gateway do aplicativo.
Esse cmdlet atribui a configuração que esse parâmetro especifica a um gateway de aplicativo.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigFile
Especifica o caminho de um arquivo de configuração, em formato XML, para um gateway de aplicativo.
Esse cmdlet atribui a configuração que esse parâmetro especifica a um gateway de aplicativo.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do gateway do aplicativo que este cmdlet configura.

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

### System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration

## EXIBE

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## INFORMA

## LINKS RELACIONADOS

[Get-AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


