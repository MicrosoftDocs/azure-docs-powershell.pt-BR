---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258824"
---
# <span data-ttu-id="a7e79-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="a7e79-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="a7e79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7e79-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e79-103">A operação para obter o histórico de execução de uma exportação para o escopo e o nome de exportação definidos.</span><span class="sxs-lookup"><span data-stu-id="a7e79-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="a7e79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7e79-104">SYNTAX</span></span>

### <span data-ttu-id="a7e79-105">Get (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7e79-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7e79-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7e79-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7e79-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7e79-107">DESCRIPTION</span></span>
<span data-ttu-id="a7e79-108">A operação para obter o histórico de execução de uma exportação para o escopo e o nome de exportação definidos.</span><span class="sxs-lookup"><span data-stu-id="a7e79-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="a7e79-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7e79-109">EXAMPLES</span></span>

### <span data-ttu-id="a7e79-110">Exemplo 1: obter AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="a7e79-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="a7e79-111">Obter AzCostManagementExportExecutionHistory de exportname e Scope</span><span class="sxs-lookup"><span data-stu-id="a7e79-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="a7e79-112">Exemplo 2: obter AzCostManagementExportExecutionHistory por InputObject</span><span class="sxs-lookup"><span data-stu-id="a7e79-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="a7e79-113">Obter AzCostManagementExportExecutionHistory por InputObject</span><span class="sxs-lookup"><span data-stu-id="a7e79-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="a7e79-114">OS</span><span class="sxs-lookup"><span data-stu-id="a7e79-114">PARAMETERS</span></span>

### <span data-ttu-id="a7e79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e79-115">-DefaultProfile</span></span>
<span data-ttu-id="a7e79-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e79-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7e79-117">-Exportname</span><span class="sxs-lookup"><span data-stu-id="a7e79-117">-ExportName</span></span>
<span data-ttu-id="a7e79-118">Nome para exportação.</span><span class="sxs-lookup"><span data-stu-id="a7e79-118">Export Name.</span></span>

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

### <span data-ttu-id="a7e79-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7e79-119">-InputObject</span></span>
<span data-ttu-id="a7e79-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a7e79-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7e79-121">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a7e79-121">-Scope</span></span>
<span data-ttu-id="a7e79-122">Esse parâmetro define o escopo de costmanagement de uma "assinatura", "Resource" e "fornecer serviço" de perspectivas diferentes.</span><span class="sxs-lookup"><span data-stu-id="a7e79-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="a7e79-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e79-123">CommonParameters</span></span>
<span data-ttu-id="a7e79-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e79-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e79-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7e79-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e79-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7e79-126">INPUTS</span></span>

### <span data-ttu-id="a7e79-127">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="a7e79-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="a7e79-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7e79-128">OUTPUTS</span></span>

### <span data-ttu-id="a7e79-129">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. Api20200601. IExportExecution</span><span class="sxs-lookup"><span data-stu-id="a7e79-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="a7e79-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7e79-130">NOTES</span></span>

<span data-ttu-id="a7e79-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a7e79-131">ALIASES</span></span>

<span data-ttu-id="a7e79-132">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a7e79-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7e79-133">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a7e79-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7e79-134">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7e79-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7e79-135">INPUTobject <ICostManagementIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a7e79-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7e79-136">`[AlertId <String>]`: ID do alerta</span><span class="sxs-lookup"><span data-stu-id="a7e79-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="a7e79-137">`[ExportName <String>]`: Exportar nome.</span><span class="sxs-lookup"><span data-stu-id="a7e79-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="a7e79-138">`[ExternalCloudProviderId <String>]`: Pode ser ' {externalSubscriptionId} ' para a conta vinculada ou ' {externalBillingAccountId} ' para a conta consolidada usada com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="a7e79-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="a7e79-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="a7e79-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="a7e79-140">Isso inclui "externalSubscriptions" para a conta vinculada e "externalBillingAccounts" para a conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="a7e79-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="a7e79-141">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a7e79-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7e79-142">`[Scope <String>]`: O escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="a7e79-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="a7e79-143">Isso inclui ' assinaturas/{SubscriptionId} ' para o escopo da assinatura, ' assinaturas/{SubscriptionId}/resourceGroups/{resourceGroupName} ' para o escopo do subsource, ' provedores/Microsoft. billing/billingAccounts/{billingAccountId} ' para o escopo da conta de cobrança, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/departamentos/{DepartmentID} ' para escopo do departamento, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} ' para escopo EnrollmentAccount, ' Providers billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' para BillingProfile Scope, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' para InvoiceSection Scope, ' Providers/Microsoft. Management/managementGroups/{managementGroupId} ' para o escopo do grupo de gerenciamento, ' Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} ' para o escopo da conta de cobrança externa e os ' provedores/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} ' para o escopo de assinatura externa.</span><span class="sxs-lookup"><span data-stu-id="a7e79-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="a7e79-144">`[ViewName <String>]`: Nome do modo de exibição</span><span class="sxs-lookup"><span data-stu-id="a7e79-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="a7e79-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7e79-145">RELATED LINKS</span></span>

