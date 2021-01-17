---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434511"
---
# Get-AzBillingAccount

## Sinopse
Obter contas de cobrança.

## SYNTAX

### Lista (padrão)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Apenas
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzBillingAccount** Obtém contas de cobrança, o usuário tem acesso a. 

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzBillingAccount
```

Obter todas as contas de cobrança às quais o usuário tem acesso.

### Exemplo 2
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

Obter a conta de cobrança com o nome especificado.

### Exemplo 3
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Obter todas as contas de cobrança às quais o usuário tem acesso e incluir o endereço no resultado.

### Exemplo 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Obter todas as contas de cobrança às quais o usuário tem acesso e incluir os perfis de cobrança no resultado.

### Exemplo 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Obter todas as contas de cobrança as quais o usuário tem acesso e incluir as seções perfis de cobrança e faturas sob elas no resultado.

### Exemplo 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Obtenha a conta de cobrança com o nome especificado e inclua o endereço, os perfis de cobrança e as seções de fatura sob eles no resultado.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeAddress
Inclua o endereço da conta de cobrança.

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

### -ExpandBillingProfile
Inclua os perfis de cobrança na conta de cobrança.

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

### -ExpandInvoiceSection
Inclua os perfis de cobrança nas seções conta de cobrança e faturas.

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

### -Nome
Nome de uma conta de cobrança específica.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListEntitiesToCreateSubscription
Liste as entidades de cobrança em conta de cobrança que podem ser usadas como entrada para criar a assinatura.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. billing. Models. PSBillingAccount

## INFORMA

## LINKS RELACIONADOS
