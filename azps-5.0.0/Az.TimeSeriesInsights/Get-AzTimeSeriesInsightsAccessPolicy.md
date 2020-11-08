---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116596"
---
# <span data-ttu-id="888df-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="888df-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="888df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="888df-102">SYNOPSIS</span></span>
<span data-ttu-id="888df-103">Obtém a política de acesso com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="888df-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="888df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="888df-104">SYNTAX</span></span>

### <span data-ttu-id="888df-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="888df-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="888df-106">Obter</span><span class="sxs-lookup"><span data-stu-id="888df-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="888df-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="888df-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="888df-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="888df-108">DESCRIPTION</span></span>
<span data-ttu-id="888df-109">Obtém a política de acesso com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="888df-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="888df-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="888df-110">EXAMPLES</span></span>

### <span data-ttu-id="888df-111">Exemplo 1: listar todas as políticas de acesso em um ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="888df-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="888df-112">Esse comando lista todas as políticas de acesso em um ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="888df-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="888df-113">Exemplo 2: obter uma política de acesso especificada por nome</span><span class="sxs-lookup"><span data-stu-id="888df-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="888df-114">Este comando obtém uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="888df-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="888df-115">Exemplo 3: obter uma política de acesso especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="888df-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="888df-116">Este comando obtém uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="888df-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="888df-117">OS</span><span class="sxs-lookup"><span data-stu-id="888df-117">PARAMETERS</span></span>

### <span data-ttu-id="888df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="888df-118">-DefaultProfile</span></span>
<span data-ttu-id="888df-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="888df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="888df-120">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="888df-120">-EnvironmentName</span></span>
<span data-ttu-id="888df-121">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="888df-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="888df-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="888df-122">-InputObject</span></span>
<span data-ttu-id="888df-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="888df-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="888df-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="888df-124">-Name</span></span>
<span data-ttu-id="888df-125">O nome da política de acesso às informações da série temporal associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="888df-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="888df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="888df-126">-ResourceGroupName</span></span>
<span data-ttu-id="888df-127">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="888df-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="888df-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="888df-128">-SubscriptionId</span></span>
<span data-ttu-id="888df-129">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="888df-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="888df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="888df-130">CommonParameters</span></span>
<span data-ttu-id="888df-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="888df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="888df-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="888df-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="888df-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="888df-133">INPUTS</span></span>

### <span data-ttu-id="888df-134">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="888df-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="888df-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="888df-135">OUTPUTS</span></span>

### <span data-ttu-id="888df-136">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="888df-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="888df-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="888df-137">NOTES</span></span>

<span data-ttu-id="888df-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="888df-138">ALIASES</span></span>

<span data-ttu-id="888df-139">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="888df-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="888df-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="888df-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="888df-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="888df-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="888df-142">INPUTobject <ITimeSeriesInsightsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="888df-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="888df-143">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="888df-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="888df-144">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="888df-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="888df-145">`[EventSourceName <String>]`: O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="888df-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="888df-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="888df-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="888df-147">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="888df-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="888df-148">`[ResourceGroupName <String>]`: Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="888df-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="888df-149">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="888df-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="888df-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="888df-150">RELATED LINKS</span></span>

