---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945536"
---
# Get-AzureTrafficManagerProfile

## Sinopse
Obtém os detalhes de um perfil do Gerenciador de tráfego.

## SYNTAX

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureTrafficManagerProfile** Obtém os detalhes de um perfil do Gerenciador de tráfego do Microsoft Azure.
Se você não especificar o parâmetro *Name* , o cmdlet listará os perfis do Gerenciador de tráfego na assinatura atual.

## EXEMPLOS

### Exemplo 1: obter a lista de perfis do Gerenciador de tráfego em uma assinatura
```
PS C:\>Get-AzureTrafficManagerProfile
```

Este comando obtém a lista de perfis do Gerenciador de tráfego na sua assinatura.

### Exemplo 2: obter um perfil do Gerenciador de tráfego
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

Esse comando obtém o perfil do Gerenciador de tráfego chamado MyProfile.

### Exemplo 3: adicionar um ponto de extremidade a um perfil do Gerenciador de tráfego
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

Esse comando adiciona um ponto de extremidade a um perfil do Gerenciador de tráfego e, em seguida, salva o perfil.

## OS

### -Nome
Especifica o nome do perfil do Gerenciador de tráfego a ser obtido.

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

## EXIBE

### Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition
Esse cmdlet gera um objeto ou objetos de perfil do Gerenciador de tráfego.

## INFORMA

## LINKS RELACIONADOS

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


