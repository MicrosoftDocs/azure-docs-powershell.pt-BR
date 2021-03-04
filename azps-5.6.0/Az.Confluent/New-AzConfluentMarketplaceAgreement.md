---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: f8c293870fa4eeb6f0df8a543473c8a9bda314c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893225"
---
# New-AzConfluentMarketplaceAgreement

## SYNOPSIS
Aceitar termos de marketplace.

## SINTAXE

```
New-AzConfluentMarketplaceAgreement [-SubscriptionId <String>] [-Accepted] [-LicenseTextLink <String>]
 [-Plan <String>] [-PrivacyPolicyLink <String>] [-Product <String>] [-Publisher <String>]
 [-RetrieveDatetime <DateTime>] [-Signature <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
Aceitar termos de marketplace.

## EXEMPLOS

### Exemplo 1: Criar contrato de marketplace confluente sob uma assinatura
```powershell
PS C:\> New-AzConfluentMarketplaceAgreement -Accepted

Name    Type
----    ----
default Microsoft.Confluent/agreement
```

Este comando cria um contrato de marketplace confluente sob uma assinatura.

## PARÂMETROS

### -Accepted
Se qualquer versão dos termos tiver sido aceita, caso contrário, false.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseTextLink
Link para HTML com termos microsoft e publisher.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plan
Planejar cadeia de caracteres de identificador.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivacyPolicyLink
Link para a política de privacidade do editor.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Product
Cadeia de caracteres do identificador do produto.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publisher
Cadeia de caracteres de identificador do publisher.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetrieveDatetime
Data e hora em UTC de quando os termos foram aceitos.
Isso será vazio se Accepted for false.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Signature
Assinatura de termos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID de assinatura do Microsoft Azure

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource

## NOTES

ALIASES

## LINKS RELACIONADOS

