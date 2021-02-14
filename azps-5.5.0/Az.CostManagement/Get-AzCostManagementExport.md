---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115891"
---
# <span data-ttu-id="75299-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="75299-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="75299-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75299-102">SYNOPSIS</span></span>
<span data-ttu-id="75299-103">A operação para obter a exportação do escopo definido por nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="75299-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="75299-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75299-104">SYNTAX</span></span>

### <span data-ttu-id="75299-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75299-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="75299-106">Obter</span><span class="sxs-lookup"><span data-stu-id="75299-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="75299-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="75299-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="75299-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="75299-108">DESCRIPTION</span></span>
<span data-ttu-id="75299-109">A operação para obter a exportação do escopo definido por nome de exportação.</span><span class="sxs-lookup"><span data-stu-id="75299-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="75299-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75299-110">EXAMPLES</span></span>

### <span data-ttu-id="75299-111">Exemplo 1: Obter todos os AzCostManagementExports por escopo</span><span class="sxs-lookup"><span data-stu-id="75299-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="75299-112">Obter todos os AzCostManagementExports por Escopo</span><span class="sxs-lookup"><span data-stu-id="75299-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="75299-113">Exemplo 2: Obter AzCostManagementExport por Nome e escopo</span><span class="sxs-lookup"><span data-stu-id="75299-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="75299-114">Obter o AzCostManagementExport por Nome e escopo</span><span class="sxs-lookup"><span data-stu-id="75299-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="75299-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75299-115">PARAMETERS</span></span>

### <span data-ttu-id="75299-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75299-116">-DefaultProfile</span></span>
<span data-ttu-id="75299-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75299-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75299-118">-Expandir</span><span class="sxs-lookup"><span data-stu-id="75299-118">-Expand</span></span>
<span data-ttu-id="75299-119">Podem ser usadas para expandir as propriedades dentro de uma exportação.</span><span class="sxs-lookup"><span data-stu-id="75299-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="75299-120">Atualmente, somente "runHistory" tem suporte e retornará informações para as últimas 10 execuções da exportação.</span><span class="sxs-lookup"><span data-stu-id="75299-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="75299-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75299-121">-InputObject</span></span>
<span data-ttu-id="75299-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="75299-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="75299-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="75299-123">-Name</span></span>
<span data-ttu-id="75299-124">Exportar Nome.</span><span class="sxs-lookup"><span data-stu-id="75299-124">Export Name.</span></span>

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

### <span data-ttu-id="75299-125">-Escopo</span><span class="sxs-lookup"><span data-stu-id="75299-125">-Scope</span></span>
<span data-ttu-id="75299-126">Este parâmetro define o escopo de gerenciamento de custos de perspectivas diferentes "Assinatura", "Grupo de Recursos" e "Fornecer Serviço".</span><span class="sxs-lookup"><span data-stu-id="75299-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="75299-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75299-127">CommonParameters</span></span>
<span data-ttu-id="75299-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75299-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75299-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75299-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75299-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="75299-130">INPUTS</span></span>

### <span data-ttu-id="75299-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="75299-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="75299-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="75299-132">OUTPUTS</span></span>

### <span data-ttu-id="75299-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="75299-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="75299-134">Notas</span><span class="sxs-lookup"><span data-stu-id="75299-134">NOTES</span></span>

<span data-ttu-id="75299-135">Aliases</span><span class="sxs-lookup"><span data-stu-id="75299-135">ALIASES</span></span>

<span data-ttu-id="75299-136">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="75299-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75299-137">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="75299-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75299-138">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75299-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75299-139">INPUTOBJECT: <ICostManagementIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="75299-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75299-140">`[AlertId <String>]`: ID de alerta</span><span class="sxs-lookup"><span data-stu-id="75299-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="75299-141">`[ExportName <String>]`: Exportar Nome.</span><span class="sxs-lookup"><span data-stu-id="75299-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="75299-142">`[ExternalCloudProviderId <String>]`: pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para contas consolidadas usadas com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="75299-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="75299-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: o tipo de provedor de nuvem externo associado às operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="75299-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="75299-144">Isso inclui "externalSubscriptions" para conta vinculada e "externalBillingAccounts" para conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="75299-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="75299-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="75299-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75299-146">`[Scope <String>]`: o escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="75299-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="75299-147">Isso inclui "assinaturas/{subscriptionId}" para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}' para escopo de Conta de Cobrança, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' para escopo do Departamento, 'provedores/Microsoft.Billing/billingAccounts/{billingAccounts}/enrollmentAccounts/{enrollmentAccountId}' para o escopo de EnrollmentAccounts, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' para escopo invoiceSection, 'provedores/Microsoft.Management/managementGroups/{managementGroupId}' para escopo do Grupo de Gerenciamento, 'provedores/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' para escopo de Conta de Cobrança Externa e 'provedores/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' para escopo de Assinatura Externa.</span><span class="sxs-lookup"><span data-stu-id="75299-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="75299-148">`[ViewName <String>]`: Nome da exibição</span><span class="sxs-lookup"><span data-stu-id="75299-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="75299-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75299-149">RELATED LINKS</span></span>

