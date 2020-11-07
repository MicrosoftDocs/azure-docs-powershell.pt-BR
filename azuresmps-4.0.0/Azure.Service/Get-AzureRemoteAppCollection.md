---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946329"
---
# Get-AzureRemoteAppCollection

## Sinopse
Recupera informações sobre uma coleção do Azure RemoteApp.

## SYNTAX

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRemoteAppCollection** recupera informações sobre coleções do Azure RemoteApp no Microsoft Azure.
Ele retorna um objeto com informações em uma coleção específica, ou se nenhuma coleção for especificada, para todas as coleções na assinatura atual.

## EXEMPLOS

### Exemplo 1: obter uma lista de todas as coleções
```
PS C:\> Get-AzureRemoteAppCollection
```

Esse comando retorna uma lista de todas as coleções do RemoteApp do Azure na assinatura.

### Exemplo 2: obter informações sobre uma coleção especificada
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

Esse comando retorna informações sobre a coleção do Azure RemoteApp chamada ContosoApps.

### Exemplo 3: obter uma lista de coleções usando um caractere curinga
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

Esse comando retorna uma lista de todas as coleções do RemoteApp do Azure correspondentes às finanças *.

## OS

### -CollectionName
Especifica o nome da coleção do Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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

## INFORMA

## LINKS RELACIONADOS

[New-AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


