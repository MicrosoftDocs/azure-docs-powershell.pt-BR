---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: f318fcf3592c0b865684df57230f73a5f22ce024
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891210"
---
# <span data-ttu-id="fb1b3-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="fb1b3-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="fb1b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1b3-103">A operação para obter a exportação para o escopo definido pelo nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="fb1b3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fb1b3-104">SYNTAX</span></span>

### <span data-ttu-id="fb1b3-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fb1b3-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb1b3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="fb1b3-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb1b3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fb1b3-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fb1b3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fb1b3-108">DESCRIPTION</span></span>
<span data-ttu-id="fb1b3-109">A operação para obter a exportação para o escopo definido pelo nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="fb1b3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb1b3-110">EXAMPLES</span></span>

### <span data-ttu-id="fb1b3-111">Exemplo 1: Obter todos os AzCostManagementExports por escopo</span><span class="sxs-lookup"><span data-stu-id="fb1b3-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="fb1b3-112">Obter todos os AzCostManagementExports por Escopo</span><span class="sxs-lookup"><span data-stu-id="fb1b3-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="fb1b3-113">Exemplo 2: Obter AzCostManagementExport por Nome e escopo</span><span class="sxs-lookup"><span data-stu-id="fb1b3-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="fb1b3-114">Obter AzCostManagementExport por Nome e escopo</span><span class="sxs-lookup"><span data-stu-id="fb1b3-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="fb1b3-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fb1b3-115">PARAMETERS</span></span>

### <span data-ttu-id="fb1b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1b3-116">-DefaultProfile</span></span>
<span data-ttu-id="fb1b3-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb1b3-118">-Expand</span><span class="sxs-lookup"><span data-stu-id="fb1b3-118">-Expand</span></span>
<span data-ttu-id="fb1b3-119">Pode ser usado para expandir as propriedades dentro de uma exportação.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="fb1b3-120">Atualmente, apenas 'runHistory' é suportado e retornará informações para as últimas 10 execuções da exportação.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="fb1b3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb1b3-121">-InputObject</span></span>
<span data-ttu-id="fb1b3-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fb1b3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fb1b3-123">-Name</span></span>
<span data-ttu-id="fb1b3-124">Nome da Exportação.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-124">Export Name.</span></span>

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

### <span data-ttu-id="fb1b3-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="fb1b3-125">-Scope</span></span>
<span data-ttu-id="fb1b3-126">Este parâmetro define o escopo de gerenciamento de custos de diferentes perspectivas 'Subscription','ResourceGroup' e 'Provide Service'.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="fb1b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1b3-127">CommonParameters</span></span>
<span data-ttu-id="fb1b3-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1b3-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb1b3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1b3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb1b3-130">INPUTS</span></span>

### <span data-ttu-id="fb1b3-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="fb1b3-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="fb1b3-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fb1b3-132">OUTPUTS</span></span>

### <span data-ttu-id="fb1b3-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="fb1b3-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="fb1b3-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="fb1b3-134">NOTES</span></span>

<span data-ttu-id="fb1b3-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fb1b3-135">ALIASES</span></span>

<span data-ttu-id="fb1b3-136">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="fb1b3-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb1b3-137">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb1b3-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb1b3-139">INPUTOBJECT <ICostManagementIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="fb1b3-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fb1b3-140">`[AlertId <String>]`: ID de alerta</span><span class="sxs-lookup"><span data-stu-id="fb1b3-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="fb1b3-141">`[ExportName <String>]`: Nome da Exportação.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="fb1b3-142">`[ExternalCloudProviderId <String>]`: Pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para conta consolidada usada com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="fb1b3-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="fb1b3-144">Isso inclui 'externalSubscriptions' para conta vinculada e 'externalBillingAccounts' para conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="fb1b3-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fb1b3-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fb1b3-146">`[Scope <String>]`: o escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="fb1b3-147">Isso inclui 'assinaturas/{subscriptionId}' para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' para escopo do Grupo de Gerenciamento, 'provedores/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' para escopo de Conta de Cobrança Externa e 'provedores/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' para escopo de Assinatura Externa.</span><span class="sxs-lookup"><span data-stu-id="fb1b3-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="fb1b3-148">`[ViewName <String>]`: Nome da exibição</span><span class="sxs-lookup"><span data-stu-id="fb1b3-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="fb1b3-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb1b3-149">RELATED LINKS</span></span>

