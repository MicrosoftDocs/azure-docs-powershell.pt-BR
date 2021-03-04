---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 20a9abc5cfc2ad2cc35bbedcf976daac286abb92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887935"
---
# <span data-ttu-id="e2512-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e2512-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="e2512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2512-102">SYNOPSIS</span></span>
<span data-ttu-id="e2512-103">Obtém a política de acesso com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="e2512-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="e2512-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e2512-104">SYNTAX</span></span>

### <span data-ttu-id="e2512-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e2512-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e2512-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e2512-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e2512-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e2512-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2512-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e2512-108">DESCRIPTION</span></span>
<span data-ttu-id="e2512-109">Obtém a política de acesso com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="e2512-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="e2512-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2512-110">EXAMPLES</span></span>

### <span data-ttu-id="e2512-111">Exemplo 1: Listar todas as políticas de acesso em um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="e2512-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e2512-112">Este comando lista todas as políticas de acesso em um ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="e2512-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="e2512-113">Exemplo 2: Obter uma política de acesso especificada pelo nome</span><span class="sxs-lookup"><span data-stu-id="e2512-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e2512-114">Este comando obtém uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="e2512-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="e2512-115">Exemplo 3: Obter uma política de acesso especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="e2512-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e2512-116">Este comando obtém uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="e2512-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="e2512-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e2512-117">PARAMETERS</span></span>

### <span data-ttu-id="e2512-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2512-118">-DefaultProfile</span></span>
<span data-ttu-id="e2512-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2512-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2512-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e2512-120">-EnvironmentName</span></span>
<span data-ttu-id="e2512-121">O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e2512-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="e2512-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2512-122">-InputObject</span></span>
<span data-ttu-id="e2512-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e2512-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2512-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e2512-124">-Name</span></span>
<span data-ttu-id="e2512-125">O nome da política de acesso do Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="e2512-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2512-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2512-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2512-127">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2512-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="e2512-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2512-128">-SubscriptionId</span></span>
<span data-ttu-id="e2512-129">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2512-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2512-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2512-130">CommonParameters</span></span>
<span data-ttu-id="e2512-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2512-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2512-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2512-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2512-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2512-133">INPUTS</span></span>

### <span data-ttu-id="e2512-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e2512-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e2512-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e2512-135">OUTPUTS</span></span>

### <span data-ttu-id="e2512-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="e2512-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="e2512-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="e2512-137">NOTES</span></span>

<span data-ttu-id="e2512-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e2512-138">ALIASES</span></span>

<span data-ttu-id="e2512-139">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e2512-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2512-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e2512-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2512-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2512-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2512-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="e2512-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2512-143">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="e2512-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e2512-144">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="e2512-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e2512-145">`[EventSourceName <String>]`: O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="e2512-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e2512-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e2512-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2512-147">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="e2512-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e2512-148">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2512-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e2512-149">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2512-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e2512-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2512-150">RELATED LINKS</span></span>

