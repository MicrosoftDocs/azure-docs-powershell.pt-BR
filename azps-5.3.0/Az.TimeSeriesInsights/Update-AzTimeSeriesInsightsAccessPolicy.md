---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272301"
---
# <span data-ttu-id="29991-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="29991-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="29991-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29991-102">SYNOPSIS</span></span>
<span data-ttu-id="29991-103">Atualiza a política de acesso com o nome especificado na assinatura especificada, no grupo de recursos e no ambiente.</span><span class="sxs-lookup"><span data-stu-id="29991-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="29991-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29991-104">SYNTAX</span></span>

### <span data-ttu-id="29991-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="29991-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="29991-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="29991-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29991-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29991-107">DESCRIPTION</span></span>
<span data-ttu-id="29991-108">Atualiza a política de acesso com o nome especificado na assinatura especificada, no grupo de recursos e no ambiente.</span><span class="sxs-lookup"><span data-stu-id="29991-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="29991-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29991-109">EXAMPLES</span></span>

### <span data-ttu-id="29991-110">Exemplo 1: atualizar uma política de acesso especificada por nome</span><span class="sxs-lookup"><span data-stu-id="29991-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="29991-111">Este comando atualiza uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="29991-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="29991-112">Exemplo 2: atualizar uma política de acesso especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="29991-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="29991-113">Este comando atualiza uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="29991-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="29991-114">OS</span><span class="sxs-lookup"><span data-stu-id="29991-114">PARAMETERS</span></span>

### <span data-ttu-id="29991-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29991-115">-DefaultProfile</span></span>
<span data-ttu-id="29991-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29991-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29991-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="29991-117">-Description</span></span>
<span data-ttu-id="29991-118">Uma descrição da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="29991-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="29991-119">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="29991-119">-EnvironmentName</span></span>
<span data-ttu-id="29991-120">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="29991-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29991-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29991-121">-InputObject</span></span>
<span data-ttu-id="29991-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="29991-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29991-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="29991-123">-Name</span></span>
<span data-ttu-id="29991-124">O nome da política de acesso às informações da série temporal associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="29991-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29991-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29991-125">-ResourceGroupName</span></span>
<span data-ttu-id="29991-126">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="29991-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29991-127">-Função</span><span class="sxs-lookup"><span data-stu-id="29991-127">-Role</span></span>
<span data-ttu-id="29991-128">A lista de funções que o principal está atribuído no ambiente.</span><span class="sxs-lookup"><span data-stu-id="29991-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29991-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29991-129">-SubscriptionId</span></span>
<span data-ttu-id="29991-130">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="29991-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29991-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29991-131">-Confirm</span></span>
<span data-ttu-id="29991-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29991-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29991-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29991-133">-WhatIf</span></span>
<span data-ttu-id="29991-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29991-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29991-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29991-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29991-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29991-136">CommonParameters</span></span>
<span data-ttu-id="29991-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29991-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29991-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29991-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29991-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29991-139">INPUTS</span></span>

### <span data-ttu-id="29991-140">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="29991-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="29991-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29991-141">OUTPUTS</span></span>

### <span data-ttu-id="29991-142">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="29991-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="29991-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29991-143">NOTES</span></span>

<span data-ttu-id="29991-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="29991-144">ALIASES</span></span>

<span data-ttu-id="29991-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="29991-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29991-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="29991-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29991-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="29991-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29991-148">INPUTobject <ITimeSeriesInsightsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="29991-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29991-149">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="29991-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="29991-150">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="29991-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="29991-151">`[EventSourceName <String>]`: O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="29991-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="29991-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="29991-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29991-153">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="29991-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="29991-154">`[ResourceGroupName <String>]`: Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="29991-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="29991-155">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="29991-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="29991-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29991-156">RELATED LINKS</span></span>

