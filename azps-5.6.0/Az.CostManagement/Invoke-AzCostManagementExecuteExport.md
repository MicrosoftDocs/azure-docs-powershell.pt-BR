---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/invoke-azcostmanagementexecuteexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
ms.openlocfilehash: ef26f52068794349b785c8c067ead33b1ee3284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889336"
---
# <span data-ttu-id="9dc4d-101">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="9dc4d-101">Invoke-AzCostManagementExecuteExport</span></span>

## <span data-ttu-id="9dc4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dc4d-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc4d-103">A operação para executar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-103">The operation to execute an export.</span></span>

## <span data-ttu-id="9dc4d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9dc4d-104">SYNTAX</span></span>

### <span data-ttu-id="9dc4d-105">Executar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9dc4d-105">Execute (Default)</span></span>
```
Invoke-AzCostManagementExecuteExport -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9dc4d-106">ExecuteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9dc4d-106">ExecuteViaIdentity</span></span>
```
Invoke-AzCostManagementExecuteExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9dc4d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9dc4d-107">DESCRIPTION</span></span>
<span data-ttu-id="9dc4d-108">A operação para executar uma exportação.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-108">The operation to execute an export.</span></span>

## <span data-ttu-id="9dc4d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9dc4d-109">EXAMPLES</span></span>

### <span data-ttu-id="9dc4d-110">Exemplo 1: Invocar Exportação por ExportName e Escopo</span><span class="sxs-lookup"><span data-stu-id="9dc4d-110">Example 1: Invoke Export by ExportName and Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementExecuteExport -ExportName 'TestExport' -Scope 'subscriptions/**********'

```

<span data-ttu-id="9dc4d-111">Invocar Exportação por ExportName e Escopo</span><span class="sxs-lookup"><span data-stu-id="9dc4d-111">Invoke Export by ExportName and Scope</span></span>

### <span data-ttu-id="9dc4d-112">Exemplo 2: Invocar Exportação por InputObject</span><span class="sxs-lookup"><span data-stu-id="9dc4d-112">Example 2: Invoke Export by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Invoke-AzCostManagementExecuteExport -InputObject $getExport

```

<span data-ttu-id="9dc4d-113">Invocar Exportar por InputObject</span><span class="sxs-lookup"><span data-stu-id="9dc4d-113">Invoke Export by InputObject</span></span>

## <span data-ttu-id="9dc4d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9dc4d-114">PARAMETERS</span></span>

### <span data-ttu-id="9dc4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc4d-115">-DefaultProfile</span></span>
<span data-ttu-id="9dc4d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dc4d-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="9dc4d-117">-ExportName</span></span>
<span data-ttu-id="9dc4d-118">Nome da Exportação.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc4d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dc4d-119">-InputObject</span></span>
<span data-ttu-id="9dc4d-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: ExecuteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc4d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dc4d-121">-PassThru</span></span>
<span data-ttu-id="9dc4d-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="9dc4d-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9dc4d-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="9dc4d-123">-Scope</span></span>
<span data-ttu-id="9dc4d-124">Este parâmetro define o escopo de gerenciamento de custos de diferentes perspectivas 'Subscription','ResourceGroup' e 'Provide Service'.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc4d-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dc4d-125">-Confirm</span></span>
<span data-ttu-id="9dc4d-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dc4d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc4d-127">-WhatIf</span></span>
<span data-ttu-id="9dc4d-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc4d-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dc4d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc4d-130">CommonParameters</span></span>
<span data-ttu-id="9dc4d-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc4d-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dc4d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc4d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dc4d-133">INPUTS</span></span>

### <span data-ttu-id="9dc4d-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="9dc4d-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="9dc4d-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9dc4d-135">OUTPUTS</span></span>

### <span data-ttu-id="9dc4d-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9dc4d-136">System.Boolean</span></span>

## <span data-ttu-id="9dc4d-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="9dc4d-137">NOTES</span></span>

<span data-ttu-id="9dc4d-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9dc4d-138">ALIASES</span></span>

<span data-ttu-id="9dc4d-139">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="9dc4d-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9dc4d-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9dc4d-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9dc4d-142">INPUTOBJECT <ICostManagementIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="9dc4d-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9dc4d-143">`[AlertId <String>]`: ID de alerta</span><span class="sxs-lookup"><span data-stu-id="9dc4d-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="9dc4d-144">`[ExportName <String>]`: Nome da Exportação.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="9dc4d-145">`[ExternalCloudProviderId <String>]`: Pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para conta consolidada usada com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="9dc4d-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="9dc4d-147">Isso inclui 'externalSubscriptions' para conta vinculada e 'externalBillingAccounts' para conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="9dc4d-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9dc4d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9dc4d-149">`[Scope <String>]`: o escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="9dc4d-150">Isso inclui 'assinaturas/{subscriptionId}' para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' para escopo do Grupo de Gerenciamento, 'provedores/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' para escopo de Conta de Cobrança Externa e 'provedores/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' para escopo de Assinatura Externa.</span><span class="sxs-lookup"><span data-stu-id="9dc4d-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="9dc4d-151">`[ViewName <String>]`: Nome da exibição</span><span class="sxs-lookup"><span data-stu-id="9dc4d-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="9dc4d-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dc4d-152">RELATED LINKS</span></span>

