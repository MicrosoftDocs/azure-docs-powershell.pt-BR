---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434003"
---
# <span data-ttu-id="81a40-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="81a40-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="81a40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81a40-102">SYNOPSIS</span></span>
<span data-ttu-id="81a40-103">A operação para obter a exportação para o escopo definido por nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="81a40-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="81a40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81a40-104">SYNTAX</span></span>

### <span data-ttu-id="81a40-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="81a40-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="81a40-106">Obter</span><span class="sxs-lookup"><span data-stu-id="81a40-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="81a40-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81a40-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="81a40-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81a40-108">DESCRIPTION</span></span>
<span data-ttu-id="81a40-109">A operação para obter a exportação para o escopo definido por nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="81a40-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="81a40-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81a40-110">EXAMPLES</span></span>

### <span data-ttu-id="81a40-111">Exemplo 1: obter todos os AzCostManagementExports por escopo</span><span class="sxs-lookup"><span data-stu-id="81a40-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="81a40-112">Obter todos os AzCostManagementExports por escopo</span><span class="sxs-lookup"><span data-stu-id="81a40-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="81a40-113">Exemplo 2: obter AzCostManagementExport por nome e escopo</span><span class="sxs-lookup"><span data-stu-id="81a40-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="81a40-114">Obter AzCostManagementExport por nome e escopo</span><span class="sxs-lookup"><span data-stu-id="81a40-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="81a40-115">OS</span><span class="sxs-lookup"><span data-stu-id="81a40-115">PARAMETERS</span></span>

### <span data-ttu-id="81a40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a40-116">-DefaultProfile</span></span>
<span data-ttu-id="81a40-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81a40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81a40-118">-Expandir</span><span class="sxs-lookup"><span data-stu-id="81a40-118">-Expand</span></span>
<span data-ttu-id="81a40-119">Pode ser usado para expandir as propriedades em uma exportação.</span><span class="sxs-lookup"><span data-stu-id="81a40-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="81a40-120">Atualmente, apenas "runHistory" tem suporte e retornará informações para as 10 últimas execuções da exportação.</span><span class="sxs-lookup"><span data-stu-id="81a40-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="81a40-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81a40-121">-InputObject</span></span>
<span data-ttu-id="81a40-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="81a40-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="81a40-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="81a40-123">-Name</span></span>
<span data-ttu-id="81a40-124">Nome para exportação.</span><span class="sxs-lookup"><span data-stu-id="81a40-124">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a40-125">-Escopo</span><span class="sxs-lookup"><span data-stu-id="81a40-125">-Scope</span></span>
<span data-ttu-id="81a40-126">Esse parâmetro define o escopo de costmanagement de uma "assinatura", "Resource" e "fornecer serviço" de perspectivas diferentes.</span><span class="sxs-lookup"><span data-stu-id="81a40-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a40-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a40-127">CommonParameters</span></span>
<span data-ttu-id="81a40-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a40-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a40-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81a40-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a40-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81a40-130">INPUTS</span></span>

### <span data-ttu-id="81a40-131">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="81a40-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="81a40-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81a40-132">OUTPUTS</span></span>

### <span data-ttu-id="81a40-133">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="81a40-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="81a40-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81a40-134">NOTES</span></span>

<span data-ttu-id="81a40-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="81a40-135">ALIASES</span></span>

<span data-ttu-id="81a40-136">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="81a40-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81a40-137">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="81a40-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81a40-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81a40-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81a40-139">INPUTobject <ICostManagementIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="81a40-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81a40-140">`[AlertId <String>]`: ID do alerta</span><span class="sxs-lookup"><span data-stu-id="81a40-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="81a40-141">`[ExportName <String>]`: Exportar nome.</span><span class="sxs-lookup"><span data-stu-id="81a40-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="81a40-142">`[ExternalCloudProviderId <String>]`: Pode ser ' {externalSubscriptionId} ' para a conta vinculada ou ' {externalBillingAccountId} ' para a conta consolidada usada com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="81a40-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="81a40-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="81a40-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="81a40-144">Isso inclui "externalSubscriptions" para a conta vinculada e "externalBillingAccounts" para a conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="81a40-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="81a40-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="81a40-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81a40-146">`[Scope <String>]`: O escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="81a40-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="81a40-147">Isso inclui ' assinaturas/{SubscriptionId} ' para o escopo da assinatura, ' assinaturas/{SubscriptionId}/resourceGroups/{resourceGroupName} ' para o escopo do subsource, ' provedores/Microsoft. billing/billingAccounts/{billingAccountId} ' para o escopo da conta de cobrança, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/departamentos/{DepartmentID} ' para escopo do departamento, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} ' para escopo EnrollmentAccount, ' Providers billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' para BillingProfile Scope, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' para InvoiceSection Scope, ' Providers/Microsoft. Management/managementGroups/{managementGroupId} ' para o escopo do grupo de gerenciamento, ' Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} ' para o escopo da conta de cobrança externa e os ' provedores/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} ' para o escopo de assinatura externa.</span><span class="sxs-lookup"><span data-stu-id="81a40-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="81a40-148">`[ViewName <String>]`: Nome do modo de exibição</span><span class="sxs-lookup"><span data-stu-id="81a40-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="81a40-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81a40-149">RELATED LINKS</span></span>

