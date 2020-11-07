---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946549"
---
# Get-AzureStorSimpleResourceContext

## Sinopse
Obtém o contexto de recurso atual.

## SYNTAX

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorSimpleResourceContext** Obtém o contexto de recurso atual.

## EXEMPLOS

### Exemplo 1: obter o contexto atual
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

O primeiro comando define o contexto atual para ser o recurso chamado Contoso63-Tsqa usando o cmdlet **Select-AzureStorSimpleResource** .

O segundo comando obtém o contexto de recurso atual.

### Exemplo 2: tentativa de obter o contexto atual
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

Esse comando obtém o contexto atual.
Neste exemplo, nenhum contexto foi definido.
O comando retorna uma mensagem que explica o problema.

## OS

### -Perfil
Especifica um perfil do Azure.

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

### Nenhuma

## EXIBE

### StorSimpleResourceContext
Esse cmdlet retorna um objeto **ResourceContext** .

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Select-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


