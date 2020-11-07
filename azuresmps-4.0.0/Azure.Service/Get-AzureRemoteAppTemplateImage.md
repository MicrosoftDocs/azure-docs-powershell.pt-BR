---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946579"
---
# Get-AzureRemoteAppTemplateImage

## Sinopse
Recupera informações sobre as imagens de modelo do Azure RemoteApp.

## SYNTAX

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRemoteAppTemplateImage** recupera informações sobre as imagens de modelo do Azure RemoteApp no Microsoft Azure.
Esse cmdlet retorna um objeto que contém informações sobre uma imagem de modelo especificada.
Se nenhuma imagem de modelo for especificada, ela recuperará informações sobre todas as imagens de modelo na assinatura atual.

## EXEMPLOS

### Exemplo 1: obter uma lista de todas as imagens de modelo
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

Esse comando retorna a lista de todas as imagens de modelo.

### Exemplo 2: recuperar informações sobre uma imagem de modelo especificada
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

Esse comando recupera informações sobre a imagem de modelo chamada ContosoApps.

## OS

### -ImageName
Especifica o nome de uma imagem de modelo do Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


