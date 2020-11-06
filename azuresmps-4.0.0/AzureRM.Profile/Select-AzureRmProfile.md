---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425920"
---
# Select-AzureRmProfile

## Sinopse
Carrega as informações de autenticação do Azure de um arquivo.

## SYNTAX

### InMemoryProfile
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### ProfileFromDisk
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Select-AzureRmProfile carrega informações de autenticação de um arquivo para definir o contexto e o ambiente do Azure.
Cmdlets que você executa na sessão atual usam essas informações para autenticar solicitações ao Azure Resource Manager.

## EXEMPLOS

### Exemplo 1: selecionando um perfil de um PSAzureProfile
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Este exemplo seleciona um perfil de um PSAzureProfile que é passado para o cmdlet.

### Exemplo 2: selecionando um perfil de um arquivo JSON
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Este exemplo seleciona um perfil de um arquivo JSON que é passado pelo cmdlet. Esse arquivo JSON pode ser criado a partir de Save-AzureRmProfile.

## OS

### -Caminho
Especifica o caminho para as informações de perfil salvas usando Save-AzureRMProfile.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### PSAzureProfile

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRMContext]()

