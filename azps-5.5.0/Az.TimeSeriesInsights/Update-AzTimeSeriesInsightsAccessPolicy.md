---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116036"
---
# <span data-ttu-id="0a0a0-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0a0a0-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="0a0a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0a0-103">Atualiza a política de acesso com o nome especificado na assinatura, grupo de recursos e ambiente especificados.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="0a0a0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a0a0-104">SYNTAX</span></span>

### <span data-ttu-id="0a0a0-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0a0a0-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0a0a0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0a0a0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0a0a0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a0a0-107">DESCRIPTION</span></span>
<span data-ttu-id="0a0a0-108">Atualiza a política de acesso com o nome especificado na assinatura, grupo de recursos e ambiente especificados.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="0a0a0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a0a0-109">EXAMPLES</span></span>

### <span data-ttu-id="0a0a0-110">Exemplo 1: Atualizar uma política de acesso especificada por nome</span><span class="sxs-lookup"><span data-stu-id="0a0a0-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="0a0a0-111">Esse comando atualiza uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="0a0a0-112">Exemplo 2: Atualizar uma política de acesso especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="0a0a0-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="0a0a0-113">Esse comando atualiza uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="0a0a0-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a0a0-114">PARAMETERS</span></span>

### <span data-ttu-id="0a0a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0a0-115">-DefaultProfile</span></span>
<span data-ttu-id="0a0a0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a0a0-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0a0a0-117">-Description</span></span>
<span data-ttu-id="0a0a0-118">Uma descrição da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="0a0a0-119">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="0a0a0-119">-EnvironmentName</span></span>
<span data-ttu-id="0a0a0-120">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="0a0a0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a0a0-121">-InputObject</span></span>
<span data-ttu-id="0a0a0-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0a0a0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a0a0-123">-Name</span></span>
<span data-ttu-id="0a0a0-124">O nome da política de acesso Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="0a0a0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0a0-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a0a0-126">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="0a0a0-127">-Função</span><span class="sxs-lookup"><span data-stu-id="0a0a0-127">-Role</span></span>
<span data-ttu-id="0a0a0-128">A lista de funções que a entidade atribuiu ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-128">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="0a0a0-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a0a0-129">-SubscriptionId</span></span>
<span data-ttu-id="0a0a0-130">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0a0a0-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0a0a0-131">-Confirm</span></span>
<span data-ttu-id="0a0a0-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a0a0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a0a0-133">-WhatIf</span></span>
<span data-ttu-id="0a0a0-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a0a0-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a0a0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0a0-136">CommonParameters</span></span>
<span data-ttu-id="0a0a0-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0a0-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a0a0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0a0-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="0a0a0-139">INPUTS</span></span>

### <span data-ttu-id="0a0a0-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="0a0a0-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="0a0a0-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="0a0a0-141">OUTPUTS</span></span>

### <span data-ttu-id="0a0a0-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="0a0a0-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="0a0a0-143">Notas</span><span class="sxs-lookup"><span data-stu-id="0a0a0-143">NOTES</span></span>

<span data-ttu-id="0a0a0-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="0a0a0-144">ALIASES</span></span>

<span data-ttu-id="0a0a0-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="0a0a0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a0a0-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a0a0-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a0a0-148">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="0a0a0-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a0a0-149">`[AccessPolicyName <String>]`: nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="0a0a0-150">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="0a0a0-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="0a0a0-151">`[EventSourceName <String>]`: o nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="0a0a0-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="0a0a0-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a0a0-153">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="0a0a0-154">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="0a0a0-155">`[SubscriptionId <String>]`: ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0a0-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0a0a0-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a0a0-156">RELATED LINKS</span></span>

