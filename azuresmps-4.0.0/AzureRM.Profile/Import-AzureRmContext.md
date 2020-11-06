---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425483"
---
# Import-AzureRmContext

## Sinopse
Carrega as informações de autenticação do Azure de um arquivo.

## SYNTAX

### InMemoryProfile
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### ProfileFromDisk
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## DESCRITIVO
O cmdlet Import-AzureRmContext carrega informações de autenticação de um arquivo para definir o contexto e o ambiente do Azure.
Cmdlets que você executa na sessão atual usam essas informações para autenticar solicitações ao Azure Resource Manager.

## EXEMPLOS

### Exemplo 1: importando um contexto de um AzureRmProfile
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Este exemplo importa um contexto de um PSAzureProfile que é passado para o cmdlet.

### Exemplo 2: importar um contexto de um arquivo JSON
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

Este exemplo seleciona um contexto de um arquivo JSON que é passado pelo cmdlet.
Esse arquivo JSON pode ser criado a partir de Import-AzureRmContext.

## OS

### -AzureContext
Especifica o contexto do Azure do qual este cmdlet lê.
Se você não especificar um contexto, esse cmdlet lerá do contexto padrão local.

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho para as informações de contexto salvas usando Save-AzureRMContext.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## SENSORES

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile
System. String

## EXIBE

### Microsoft. Azure. Commands. Profile. Models. PSAzureProfile

## INFORMA

## LINKS RELACIONADOS

