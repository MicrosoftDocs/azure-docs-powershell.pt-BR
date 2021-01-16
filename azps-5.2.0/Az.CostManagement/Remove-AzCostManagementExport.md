---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258812"
---
# <span data-ttu-id="60f00-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="60f00-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="60f00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60f00-102">SYNOPSIS</span></span>
<span data-ttu-id="60f00-103">A operação para excluir uma exportação.</span><span class="sxs-lookup"><span data-stu-id="60f00-103">The operation to delete a export.</span></span>

## <span data-ttu-id="60f00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60f00-104">SYNTAX</span></span>

### <span data-ttu-id="60f00-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="60f00-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="60f00-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="60f00-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60f00-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60f00-107">DESCRIPTION</span></span>
<span data-ttu-id="60f00-108">A operação para excluir uma exportação.</span><span class="sxs-lookup"><span data-stu-id="60f00-108">The operation to delete a export.</span></span>

## <span data-ttu-id="60f00-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60f00-109">EXAMPLES</span></span>

### <span data-ttu-id="60f00-110">Exemplo 1: excluir o AzCostManagementExport por escopo e nome</span><span class="sxs-lookup"><span data-stu-id="60f00-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="60f00-111">Excluir o AzCostManagementExport por Scope e exportname</span><span class="sxs-lookup"><span data-stu-id="60f00-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="60f00-112">Exemplo 2: excluir o AzCostManagementExport por objeto de exportação</span><span class="sxs-lookup"><span data-stu-id="60f00-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="60f00-113">Excluir o AzCostManagementExport por InputObject</span><span class="sxs-lookup"><span data-stu-id="60f00-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="60f00-114">OS</span><span class="sxs-lookup"><span data-stu-id="60f00-114">PARAMETERS</span></span>

### <span data-ttu-id="60f00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f00-115">-DefaultProfile</span></span>
<span data-ttu-id="60f00-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60f00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f00-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60f00-117">-InputObject</span></span>
<span data-ttu-id="60f00-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="60f00-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60f00-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="60f00-119">-Name</span></span>
<span data-ttu-id="60f00-120">Nome para exportação.</span><span class="sxs-lookup"><span data-stu-id="60f00-120">Export Name.</span></span>

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

### <span data-ttu-id="60f00-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60f00-121">-PassThru</span></span>
<span data-ttu-id="60f00-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="60f00-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="60f00-123">-Escopo</span><span class="sxs-lookup"><span data-stu-id="60f00-123">-Scope</span></span>
<span data-ttu-id="60f00-124">Esse parâmetro define o escopo de costmanagement de uma "assinatura", "Resource" e "fornecer serviço" de perspectivas diferentes.</span><span class="sxs-lookup"><span data-stu-id="60f00-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="60f00-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60f00-125">-Confirm</span></span>
<span data-ttu-id="60f00-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60f00-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f00-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f00-127">-WhatIf</span></span>
<span data-ttu-id="60f00-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60f00-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f00-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60f00-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f00-130">CommonParameters</span></span>
<span data-ttu-id="60f00-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f00-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60f00-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f00-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60f00-133">INPUTS</span></span>

### <span data-ttu-id="60f00-134">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="60f00-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="60f00-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60f00-135">OUTPUTS</span></span>

### <span data-ttu-id="60f00-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60f00-136">System.Boolean</span></span>

## <span data-ttu-id="60f00-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60f00-137">NOTES</span></span>

<span data-ttu-id="60f00-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="60f00-138">ALIASES</span></span>

<span data-ttu-id="60f00-139">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="60f00-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60f00-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="60f00-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60f00-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60f00-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60f00-142">INPUTobject <ICostManagementIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="60f00-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60f00-143">`[AlertId <String>]`: ID do alerta</span><span class="sxs-lookup"><span data-stu-id="60f00-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="60f00-144">`[ExportName <String>]`: Exportar nome.</span><span class="sxs-lookup"><span data-stu-id="60f00-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="60f00-145">`[ExternalCloudProviderId <String>]`: Pode ser ' {externalSubscriptionId} ' para a conta vinculada ou ' {externalBillingAccountId} ' para a conta consolidada usada com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="60f00-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="60f00-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="60f00-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="60f00-147">Isso inclui "externalSubscriptions" para a conta vinculada e "externalBillingAccounts" para a conta consolidada.</span><span class="sxs-lookup"><span data-stu-id="60f00-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="60f00-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="60f00-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60f00-149">`[Scope <String>]`: O escopo associado às operações de exibição.</span><span class="sxs-lookup"><span data-stu-id="60f00-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="60f00-150">Isso inclui ' assinaturas/{SubscriptionId} ' para o escopo da assinatura, ' assinaturas/{SubscriptionId}/resourceGroups/{resourceGroupName} ' para o escopo do subsource, ' provedores/Microsoft. billing/billingAccounts/{billingAccountId} ' para o escopo da conta de cobrança, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/departamentos/{DepartmentID} ' para escopo do departamento, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} ' para escopo EnrollmentAccount, ' Providers billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' para BillingProfile Scope, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' para InvoiceSection Scope, ' Providers/Microsoft. Management/managementGroups/{managementGroupId} ' para o escopo do grupo de gerenciamento, ' Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} ' para o escopo da conta de cobrança externa e os ' provedores/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} ' para o escopo de assinatura externa.</span><span class="sxs-lookup"><span data-stu-id="60f00-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="60f00-151">`[ViewName <String>]`: Nome do modo de exibição</span><span class="sxs-lookup"><span data-stu-id="60f00-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="60f00-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60f00-152">RELATED LINKS</span></span>

