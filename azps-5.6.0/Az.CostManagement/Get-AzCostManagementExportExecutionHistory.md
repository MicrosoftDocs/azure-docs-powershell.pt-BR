---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 602797e32e5d29e3dd4ff2b6ade75ff8055efd0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892861"
---
# <span data-ttu-id="8e9df-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="8e9df-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="8e9df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e9df-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9df-103">A operação para obter o histórico de execução de uma exportação para o escopo definido e o nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="8e9df-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="8e9df-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8e9df-104">SYNTAX</span></span>

### <span data-ttu-id="8e9df-105">Get (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8e9df-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e9df-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e9df-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e9df-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8e9df-107">DESCRIPTION</span></span>
<span data-ttu-id="8e9df-108">A operação para obter o histórico de execução de uma exportação para o escopo definido e o nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="8e9df-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="8e9df-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e9df-109">EXAMPLES</span></span>

### <span data-ttu-id="8e9df-110">Exemplo 1: Obter AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="8e9df-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="8e9df-111">Obter AzCostManagementExportExecutionHistory por ExportName e Scope</span><span class="sxs-lookup"><span data-stu-id="8e9df-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="8e9df-112">Exemplo 2: Obter AzCostManagementExportExecutionHistory por InputObject</span><span class="sxs-lookup"><span data-stu-id="8e9df-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="8e9df-113">Obter AzCostManagementExportExecutionHistory por InputObject</span><span class="sxs-lookup"><span data-stu-id="8e9df-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="8e9df-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8e9df-114">PARAMETERS</span></span>

### <span data-ttu-id="8e9df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9df-115">-DefaultProfile</span></span>
<span data-ttu-id="8e9df-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e9df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e9df-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="8e9df-117">-ExportName</span></span>
<span data-ttu-id="8e9df-118">Nome da Exportação.</span><span class="sxs-lookup"><span data-stu-id="8e9df-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9df-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e9df-119">-InputObject</span></span>
<span data-ttu-id="8e9df-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8e9df-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9df-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="8e9df-121">-Scope</span></span>
<span data-ttu-id="8e9df-122">Este parâmetro define o escopo de gerenciamento de custos de diferentes perspectivas 'Subscription','ResourceGroup' e 'Provide Service'.</span><span class="sxs-lookup"><span data-stu-id="8e9df-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9df-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9df-123">CommonParameters</span></span>
<span data-ttu-id="8e9df-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9df-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9df-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e9df-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9df-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e9df-126">INPUTS</span></span>

### <span data-ttu-id="8e9df-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="8e9df-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="8e9df-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8e9df-128">OUTPUTS</span></span>

### <span data-ttu-id="8e9df-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="8e9df-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="8e9df-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="8e9df-130">NOTES</span></span>

<span data-ttu-id="8e9df-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8e9df-131">ALIASES</span></span>

<span data-ttu-id="8e9df-132">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="8e9df-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e9df-133">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8e9df-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e9df-134">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e9df-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e9df-135">INPUTOBJECT <ICostManagementIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="8e9df-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e9df-136">`[AlertId <String>]`: ID de alerta</span><span class="sxs-lookup"><span data-stu-id="8e9df-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="8e9df-137">`[ExportName <String>]`: Nome da Exportação.</span><span class="sxs-lookup"><span data-stu-id="8e9df-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="8e9df-138">`[ExternalCloudProviderId <String>]`: Pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para conta consolidada usada com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="8e9df-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="8e9df-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="8e9df-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="8e9df-140">Isso inclui 'externalSubscriptions' para conta vinculada e 'externalBillingAccounts' para conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="8e9df-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="8e9df-141">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8e9df-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e9df-142">`[Scope <String>]`: o escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="8e9df-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="8e9df-143">Isso inclui 'assinaturas/{subscriptionId}' para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' para escopo do Grupo de Gerenciamento, 'provedores/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' para escopo de Conta de Cobrança Externa e 'provedores/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' para escopo de Assinatura Externa.</span><span class="sxs-lookup"><span data-stu-id="8e9df-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="8e9df-144">`[ViewName <String>]`: Nome da exibição</span><span class="sxs-lookup"><span data-stu-id="8e9df-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="8e9df-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e9df-145">RELATED LINKS</span></span>

