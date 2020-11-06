---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425843"
---
# Get-AzureRmContext

## Sinopse
Obtém os metadados usados para autenticar solicitações do Azure Resource Manager.

## SYNTAX

```
Get-AzureRmContext [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzureRmContext Obtém os metadados atuais usados para autenticar solicitações do Azure Resource Manager.

Esse cmdlet obtém a conta do Active Directory, o locatário do Active Directory, a assinatura do Azure e o ambiente de destino do Azure.
Os cmdlets do Azure Resource Manager usam essas configurações por padrão ao realizar solicitações do Azure Resource Manager.

## EXEMPLOS

### Exemplo 1: obtendo o contexto atual
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Neste exemplo, estamos nos conectando à nossa conta com uma assinatura do Azure usando Add-AzureRmAccount e, em seguida, estamos obtendo o contexto da sessão atual chamando Get-AzureRmContext.

## OS

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### PSAzureContext
Esse cmdlet retorna a conta, o locatário e a assinatura usadas pelos cmdlets do Azure Resource Manager.

## INFORMA

## LINKS RELACIONADOS

[Set-AzureRMContext]()

