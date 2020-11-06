---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425919"
---
# Set-AzureRmContext

## Sinopse
Define o locatário, a assinatura e o ambiente para cmdlets a serem usados na sessão atual.

## SYNTAX

### Subscriptionname (padrão)
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Atalho
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SubscriptionId
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Set-AzureRmContext define informações de autenticação para cmdlets que você executa na sessão atual.
O contexto inclui informações de locatário, assinatura e ambiente.

## EXEMPLOS

### Exemplo 1: definir o contexto da assinatura
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

Este comando define o contexto para usar a assinatura especificada.

## OS

### -Contexto
Especifica o contexto da sessão atual.

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SubscriptionId
Especifica a ID da assinatura para o contexto que este cmdlet define para a sessão atual.

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
Especifica o nome da assinatura para o contexto que este cmdlet define para a sessão atual.

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tenantid
Especifica a ID do locatário para o contexto que este cmdlet define para a sessão atual.

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### PSAzureContext

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRMContext]()

