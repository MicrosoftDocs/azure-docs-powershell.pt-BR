---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112020"
---
# <span data-ttu-id="8eeee-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="8eeee-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="8eeee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8eeee-102">SYNOPSIS</span></span>
<span data-ttu-id="8eeee-103">A operação para obter o histórico de execução de uma exportação para o escopo definido e o nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="8eeee-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="8eeee-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8eeee-104">SYNTAX</span></span>

### <span data-ttu-id="8eeee-105">Obter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8eeee-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8eeee-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8eeee-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8eeee-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8eeee-107">DESCRIPTION</span></span>
<span data-ttu-id="8eeee-108">A operação para obter o histórico de execução de uma exportação para o escopo definido e o nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="8eeee-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="8eeee-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8eeee-109">EXAMPLES</span></span>

### <span data-ttu-id="8eeee-110">Exemplo 1: Obter AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="8eeee-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="8eeee-111">Obter AzCostManagementExportExecutionHistory By ExportName e Scope</span><span class="sxs-lookup"><span data-stu-id="8eeee-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="8eeee-112">Exemplo 2: Obter AzCostManagementExportExecutionHistory por InputObject</span><span class="sxs-lookup"><span data-stu-id="8eeee-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="8eeee-113">Obter AzCostManagementExportExecutionHistory by InputObject</span><span class="sxs-lookup"><span data-stu-id="8eeee-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="8eeee-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8eeee-114">PARAMETERS</span></span>

### <span data-ttu-id="8eeee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eeee-115">-DefaultProfile</span></span>
<span data-ttu-id="8eeee-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8eeee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eeee-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="8eeee-117">-ExportName</span></span>
<span data-ttu-id="8eeee-118">Exportar Nome.</span><span class="sxs-lookup"><span data-stu-id="8eeee-118">Export Name.</span></span>

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

### <span data-ttu-id="8eeee-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eeee-119">-InputObject</span></span>
<span data-ttu-id="8eeee-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="8eeee-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8eeee-121">-Escopo</span><span class="sxs-lookup"><span data-stu-id="8eeee-121">-Scope</span></span>
<span data-ttu-id="8eeee-122">Este parâmetro define o escopo de gerenciamento de custos de perspectivas diferentes "Assinatura", "Grupo de Recursos" e "Fornecer Serviço".</span><span class="sxs-lookup"><span data-stu-id="8eeee-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="8eeee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eeee-123">CommonParameters</span></span>
<span data-ttu-id="8eeee-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eeee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eeee-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8eeee-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eeee-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="8eeee-126">INPUTS</span></span>

### <span data-ttu-id="8eeee-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="8eeee-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="8eeee-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="8eeee-128">OUTPUTS</span></span>

### <span data-ttu-id="8eeee-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="8eeee-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="8eeee-130">Notas</span><span class="sxs-lookup"><span data-stu-id="8eeee-130">NOTES</span></span>

<span data-ttu-id="8eeee-131">Aliases</span><span class="sxs-lookup"><span data-stu-id="8eeee-131">ALIASES</span></span>

<span data-ttu-id="8eeee-132">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="8eeee-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8eeee-133">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8eeee-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8eeee-134">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8eeee-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8eeee-135">INPUTOBJECT: <ICostManagementIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="8eeee-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8eeee-136">`[AlertId <String>]`: ID de alerta</span><span class="sxs-lookup"><span data-stu-id="8eeee-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="8eeee-137">`[ExportName <String>]`: Exportar Nome.</span><span class="sxs-lookup"><span data-stu-id="8eeee-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="8eeee-138">`[ExternalCloudProviderId <String>]`: pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para contas consolidadas usadas com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="8eeee-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="8eeee-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: o tipo de provedor de nuvem externo associado às operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="8eeee-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="8eeee-140">Isso inclui "externalSubscriptions" para conta vinculada e "externalBillingAccounts" para conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="8eeee-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="8eeee-141">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="8eeee-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8eeee-142">`[Scope <String>]`: o escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="8eeee-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="8eeee-143">Isso inclui "assinaturas/{subscriptionId}" para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}' para escopo de Conta de Cobrança, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' para escopo do Departamento, 'provedores/Microsoft.Billing/billingAccounts/{billingAccounts}/enrollmentAccounts/{enrollmentAccountId}' para o escopo de EnrollmentAccounts, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' para escopo invoiceSection, 'provedores/Microsoft.Management/managementGroups/{managementGroupId}' para escopo do Grupo de Gerenciamento, 'provedores/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' para escopo de Conta de Cobrança Externa e 'provedores/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' para escopo de Assinatura Externa.</span><span class="sxs-lookup"><span data-stu-id="8eeee-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="8eeee-144">`[ViewName <String>]`: Nome da exibição</span><span class="sxs-lookup"><span data-stu-id="8eeee-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="8eeee-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eeee-145">RELATED LINKS</span></span>

