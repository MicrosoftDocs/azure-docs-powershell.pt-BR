---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946051"
---
# Set-AzureRemoteAppWorkspace

## Sinopse
Define as propriedades de um espaço de trabalho do RemoteApp do Azure.

## SYNTAX

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRemoteAppWorkspace** define as propriedades de um espaço de trabalho do Azure RemoteApp.

## EXEMPLOS

### Exemplo 1: definir o nome do espaço de trabalho
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

Esse comando define o nome do espaço de trabalho do RemoteApp do Azure para aplicativos de trabalho da contoso.

## OS

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

### -WorkspaceName
Especifica o nome do espaço de trabalho do RemoteApp do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA
* Todas as coleções do RemoteApp do Azure para uma assinatura especificada existem dentro de um espaço de trabalho compartilhado.

## LINKS RELACIONADOS

[Get-AzureRemoteAppWorkspace](./Get-AzureRemoteAppWorkspace.md)


