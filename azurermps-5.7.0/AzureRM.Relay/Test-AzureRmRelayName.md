---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431635"
---
# Test-AzureRmRelayName

## Sinopse
Verifica a disponibilidade do nome do NameSpace especificado

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Test-AzureRmRelayName** verifica a disponibilidade do nome do namespace

## EXEMPLOS

### Exemplo 1
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### Exemplo 2
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### Exemplo 3
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

Retorna o status na disponibilidade do nome do namespace

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Nome do namespace de retransmissão.

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

### [Microsoft. Azure. Commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]

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

