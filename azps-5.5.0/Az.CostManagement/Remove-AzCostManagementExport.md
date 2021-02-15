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
# <span data-ttu-id="f6039-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="f6039-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="f6039-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6039-102">SYNOPSIS</span></span>
<span data-ttu-id="f6039-103">A operação para excluir uma exportação.</span><span class="sxs-lookup"><span data-stu-id="f6039-103">The operation to delete a export.</span></span>

## <span data-ttu-id="f6039-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6039-104">SYNTAX</span></span>

### <span data-ttu-id="f6039-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f6039-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6039-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6039-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f6039-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6039-107">DESCRIPTION</span></span>
<span data-ttu-id="f6039-108">A operação para excluir uma exportação.</span><span class="sxs-lookup"><span data-stu-id="f6039-108">The operation to delete a export.</span></span>

## <span data-ttu-id="f6039-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6039-109">EXAMPLES</span></span>

### <span data-ttu-id="f6039-110">Exemplo 1: Excluir o AzCostManagementExport por Escopo e Nome</span><span class="sxs-lookup"><span data-stu-id="f6039-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="f6039-111">Excluir o AzCostManagementExport by Scope e ExportName</span><span class="sxs-lookup"><span data-stu-id="f6039-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="f6039-112">Exemplo 2: Excluir o AzCostManagementExport por Objeto de Exportação</span><span class="sxs-lookup"><span data-stu-id="f6039-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="f6039-113">Excluir o AzCostManagementExport by InputObject</span><span class="sxs-lookup"><span data-stu-id="f6039-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="f6039-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6039-114">PARAMETERS</span></span>

### <span data-ttu-id="f6039-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6039-115">-DefaultProfile</span></span>
<span data-ttu-id="f6039-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6039-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6039-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6039-117">-InputObject</span></span>
<span data-ttu-id="f6039-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f6039-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6039-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6039-119">-Name</span></span>
<span data-ttu-id="f6039-120">Exportar Nome.</span><span class="sxs-lookup"><span data-stu-id="f6039-120">Export Name.</span></span>

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

### <span data-ttu-id="f6039-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6039-121">-PassThru</span></span>
<span data-ttu-id="f6039-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f6039-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f6039-123">-Escopo</span><span class="sxs-lookup"><span data-stu-id="f6039-123">-Scope</span></span>
<span data-ttu-id="f6039-124">Este parâmetro define o escopo de gerenciamento de custos de perspectivas diferentes "Assinatura", "Grupo de Recursos" e "Fornecer Serviço".</span><span class="sxs-lookup"><span data-stu-id="f6039-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="f6039-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f6039-125">-Confirm</span></span>
<span data-ttu-id="f6039-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6039-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6039-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6039-127">-WhatIf</span></span>
<span data-ttu-id="f6039-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f6039-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6039-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6039-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6039-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6039-130">CommonParameters</span></span>
<span data-ttu-id="f6039-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6039-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6039-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6039-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6039-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="f6039-133">INPUTS</span></span>

### <span data-ttu-id="f6039-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="f6039-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="f6039-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="f6039-135">OUTPUTS</span></span>

### <span data-ttu-id="f6039-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6039-136">System.Boolean</span></span>

## <span data-ttu-id="f6039-137">Notas</span><span class="sxs-lookup"><span data-stu-id="f6039-137">NOTES</span></span>

<span data-ttu-id="f6039-138">Aliases</span><span class="sxs-lookup"><span data-stu-id="f6039-138">ALIASES</span></span>

<span data-ttu-id="f6039-139">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="f6039-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6039-140">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f6039-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6039-141">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6039-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6039-142">INPUTOBJECT: <ICostManagementIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="f6039-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6039-143">`[AlertId <String>]`: ID de alerta</span><span class="sxs-lookup"><span data-stu-id="f6039-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="f6039-144">`[ExportName <String>]`: Exportar Nome.</span><span class="sxs-lookup"><span data-stu-id="f6039-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="f6039-145">`[ExternalCloudProviderId <String>]`: pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para contas consolidadas usadas com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="f6039-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="f6039-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: o tipo de provedor de nuvem externo associado às operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="f6039-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="f6039-147">Isso inclui "externalSubscriptions" para conta vinculada e "externalBillingAccounts" para conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="f6039-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="f6039-148">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="f6039-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6039-149">`[Scope <String>]`: o escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="f6039-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="f6039-150">Isso inclui "assinaturas/{subscriptionId}" para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}' para escopo de Conta de Cobrança, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' para escopo do Departamento, 'provedores/Microsoft.Billing/billingAccounts/{billingAccounts}/enrollmentAccounts/{enrollmentAccountId}' para o escopo de EnrollmentAccounts, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' para escopo invoiceSection, 'provedores/Microsoft.Management/managementGroups/{managementGroupId}' para escopo do Grupo de Gerenciamento, 'provedores/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' para escopo de Conta de Cobrança Externa e 'provedores/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' para escopo de Assinatura Externa.</span><span class="sxs-lookup"><span data-stu-id="f6039-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="f6039-151">`[ViewName <String>]`: Nome da exibição</span><span class="sxs-lookup"><span data-stu-id="f6039-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="f6039-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6039-152">RELATED LINKS</span></span>

