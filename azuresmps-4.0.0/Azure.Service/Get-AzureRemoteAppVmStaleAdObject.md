---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945630"
---
# Get-AzureRemoteAppVmStaleAdObject

## Sinopse
Obtém objetos no Azure Active Directory associados a máquinas virtuais do Azure RemoteApp que não existem mais.

## SYNTAX

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRemoteAppVmStaleAdObject** obtém objetos do Azure Active Directory associados a máquinas virtuais do Azure RemoteApp que não existem mais.
Esse cmdlet exibe o nome de cada objeto que ele obtém.

## EXEMPLOS

### Exemplo 1: obter objetos obsoletos para uma coleção
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

Este segundo comando obtém os objetos obsoletos da coleção chamada contoso.

## OS

### -CollectionName
Especifica o nome da coleção do Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
Especifica uma credencial que tem direitos para executar esta ação.
Para obter um objeto **PSCredential** , use o cmdlet **Get-Credential** .
Se você não especificar esse parâmetro, esse cmdlet usará as credenciais do usuário atual.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## EXIBE

### String

## INFORMA

## LINKS RELACIONADOS

[Clear-AzureRemoteAppVmStaleAdObject](./Clear-AzureRemoteAppVmStaleAdObject.md)


