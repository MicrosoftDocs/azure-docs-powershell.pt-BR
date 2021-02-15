---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112008"
---
# Remove-AzCostManagementExport

## Sinopse
A operação para excluir uma exportação.

## Sintaxe

### Excluir (Padrão)
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Descrição
A operação para excluir uma exportação.

## Exemplos

### Exemplo 1: Excluir o AzCostManagementExport por Escopo e Nome
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

Excluir o AzCostManagementExport by Scope e ExportName

### Exemplo 2: Excluir o AzCostManagementExport por Objeto de Exportação
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

Excluir o AzCostManagementExport by InputObject

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -InputObject
Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Exportar Nome.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Retorna verdadeiro quando o comando é bem-sucedido

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

### -Escopo
Este parâmetro define o escopo de gerenciamento de custos de perspectivas diferentes "Assinatura", "Grupo de Recursos" e "Fornecer Serviço".

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

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
Mostra o que acontece se o cmdlet for executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity

## Saídas

### System.Boolean

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT: <ICostManagementIdentity> Parâmetro de Identidade
  - `[AlertId <String>]`: ID de alerta
  - `[ExportName <String>]`: Exportar Nome.
  - `[ExternalCloudProviderId <String>]`: pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para contas consolidadas usadas com operações de dimensão/consulta.
  - `[ExternalCloudProviderType <ExternalCloudProviderType?>]`: o tipo de provedor de nuvem externo associado às operações de dimensão/consulta. Isso inclui "externalSubscriptions" para conta vinculada e "externalBillingAccounts" para conta consolidada.
  - `[Id <String>]`: Caminho de identidade de recursos
  - `[Scope <String>]`: o escopo associado às operações de exibição. Isso inclui "assinaturas/{subscriptionId}" para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}' para escopo de Conta de Cobrança, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' para escopo do Departamento, 'provedores/Microsoft.Billing/billingAccounts/{billingAccounts}/enrollmentAccounts/{enrollmentAccountId}' para o escopo de EnrollmentAccounts, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' para escopo invoiceSection, 'provedores/Microsoft.Management/managementGroups/{managementGroupId}' para escopo do Grupo de Gerenciamento, 'provedores/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' para escopo de Conta de Cobrança Externa e 'provedores/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' para escopo de Assinatura Externa.
  - `[ViewName <String>]`: Nome da exibição

## LINKS RELACIONADOS

