---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610167"
---
# Test-AzureRmServiceBusName

## Sinopse
Verifica a disponibilidade do nome do NameSpace especificado

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## DESCRITIVO
O cmdlet **Test-AzureRmServiceBusName** verifica a disponibilidade do nome do namespace

## EXEMPLOS

### Exemplo 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### Exemplo 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### Exemplo 3
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

Retorna o status na disponibilidade do nome do namespace

## OS

### -Namespace
Nome do namespace do ServiceBus.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### -Namespace
 System. String

## EXIBE

### [Microsoft. Azure. Commands. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]

### Exemplo 1
Mensagem do motivo NameAvailable
------------- ------ -------
         True   None

### Exemplo 2
Mensagem do motivo NameAvailable
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### Exemplo 3
Mensagem do motivo NameAvailable
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## INFORMA

## LINKS RELACIONADOS
