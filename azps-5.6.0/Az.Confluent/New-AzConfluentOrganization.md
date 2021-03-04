---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
ms.openlocfilehash: 546b4e56f2a932a6d7f17bda8484db8cd1c3c593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893223"
---
# New-AzConfluentOrganization

## SYNOPSIS
Criar recurso Organization

## SINTAXE

```
New-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Location <String>] [-OfferDetailId <String>] [-OfferDetailPlanId <String>] [-OfferDetailPlanName <String>]
 [-OfferDetailPublisherId <String>] [-OfferDetailStatus <SaaSOfferStatus>] [-OfferDetailTermUnit <String>]
 [-Tag <Hashtable>] [-UserDetailEmailAddress <String>] [-UserDetailFirstName <String>]
 [-UserDetailLastName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
Criar recurso Organization

## EXEMPLOS

### Exemplo 1: Criar uma organização confluente
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" -UserDetailEmailAddress "xxxx@microsoft.com"

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

Este comando cria uma organização confluente.

## PARÂMETROS

### -AsJob
Executar o comando como um trabalho

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

### -Location
Local do recurso Organization

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

### -Name
Nome do recurso da organização

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Executar o comando de forma assíncrona

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

### -OfferDetailId
Id da oferta

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

### -OfferDetailPlanId
Id do Plano de Oferta

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

### -OfferDetailPlanName
Nome do Plano de Oferta

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

### -OfferDetailPublisherId
Publisher Id

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

### -OfferDetailStatus
Status da oferta saas

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Support.SaaSOfferStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OfferDetailTermUnit
Unidade De Termos de Plano de Oferta

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

### -ResourceGroupName
Nome do grupo de recursos

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### -Tag
Marcas de recurso da organização

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDetailEmailAddress
Endereço de email

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

### -UserDetailFirstName
Nome

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

### -UserDetailLastName
Sobrenome

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

### Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource

## NOTES

ALIASES

## LINKS RELACIONADOS

