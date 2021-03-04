---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: e3c464ee8a2ae038a9e6d8d7578c3e4862c16460
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886687"
---
# <span data-ttu-id="35848-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="35848-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="35848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35848-102">SYNOPSIS</span></span>
<span data-ttu-id="35848-103">A operação para excluir uma exportação.</span><span class="sxs-lookup"><span data-stu-id="35848-103">The operation to delete a export.</span></span>

## <span data-ttu-id="35848-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="35848-104">SYNTAX</span></span>

### <span data-ttu-id="35848-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="35848-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35848-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35848-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35848-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="35848-107">DESCRIPTION</span></span>
<span data-ttu-id="35848-108">A operação para excluir uma exportação.</span><span class="sxs-lookup"><span data-stu-id="35848-108">The operation to delete a export.</span></span>

## <span data-ttu-id="35848-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35848-109">EXAMPLES</span></span>

### <span data-ttu-id="35848-110">Exemplo 1: Excluir o AzCostManagementExport por Escopo e Nome</span><span class="sxs-lookup"><span data-stu-id="35848-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="35848-111">Excluir o AzCostManagementExport By Scope e ExportName</span><span class="sxs-lookup"><span data-stu-id="35848-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="35848-112">Exemplo 2: Excluir o AzCostManagementExport por Objeto Export</span><span class="sxs-lookup"><span data-stu-id="35848-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="35848-113">Excluir o AzCostManagementExport By InputObject</span><span class="sxs-lookup"><span data-stu-id="35848-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="35848-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="35848-114">PARAMETERS</span></span>

### <span data-ttu-id="35848-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35848-115">-DefaultProfile</span></span>
<span data-ttu-id="35848-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35848-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35848-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35848-117">-InputObject</span></span>
<span data-ttu-id="35848-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="35848-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35848-119">-Name</span><span class="sxs-lookup"><span data-stu-id="35848-119">-Name</span></span>
<span data-ttu-id="35848-120">Nome da Exportação.</span><span class="sxs-lookup"><span data-stu-id="35848-120">Export Name.</span></span>

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

### <span data-ttu-id="35848-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35848-121">-PassThru</span></span>
<span data-ttu-id="35848-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="35848-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="35848-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="35848-123">-Scope</span></span>
<span data-ttu-id="35848-124">Este parâmetro define o escopo de gerenciamento de custos de diferentes perspectivas 'Subscription','ResourceGroup' e 'Provide Service'.</span><span class="sxs-lookup"><span data-stu-id="35848-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="35848-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35848-125">-Confirm</span></span>
<span data-ttu-id="35848-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35848-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35848-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35848-127">-WhatIf</span></span>
<span data-ttu-id="35848-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35848-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35848-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35848-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35848-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35848-130">CommonParameters</span></span>
<span data-ttu-id="35848-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35848-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35848-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35848-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35848-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35848-133">INPUTS</span></span>

### <span data-ttu-id="35848-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="35848-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="35848-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="35848-135">OUTPUTS</span></span>

### <span data-ttu-id="35848-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35848-136">System.Boolean</span></span>

## <span data-ttu-id="35848-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="35848-137">NOTES</span></span>

<span data-ttu-id="35848-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="35848-138">ALIASES</span></span>

<span data-ttu-id="35848-139">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="35848-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35848-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="35848-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35848-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35848-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35848-142">INPUTOBJECT <ICostManagementIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="35848-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35848-143">`[AlertId <String>]`: ID de alerta</span><span class="sxs-lookup"><span data-stu-id="35848-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="35848-144">`[ExportName <String>]`: Nome da Exportação.</span><span class="sxs-lookup"><span data-stu-id="35848-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="35848-145">`[ExternalCloudProviderId <String>]`: Pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para conta consolidada usada com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="35848-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="35848-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="35848-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="35848-147">Isso inclui 'externalSubscriptions' para conta vinculada e 'externalBillingAccounts' para conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="35848-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="35848-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="35848-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35848-149">`[Scope <String>]`: o escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="35848-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="35848-150">Isso inclui 'assinaturas/{subscriptionId}' para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' para escopo do Grupo de Gerenciamento, 'provedores/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' para escopo de Conta de Cobrança Externa e 'provedores/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' para escopo de Assinatura Externa.</span><span class="sxs-lookup"><span data-stu-id="35848-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="35848-151">`[ViewName <String>]`: Nome da exibição</span><span class="sxs-lookup"><span data-stu-id="35848-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="35848-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35848-152">RELATED LINKS</span></span>

