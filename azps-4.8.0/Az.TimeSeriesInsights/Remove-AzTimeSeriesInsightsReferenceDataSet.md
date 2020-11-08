---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110718"
---
# <span data-ttu-id="481e5-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="481e5-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="481e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="481e5-102">SYNOPSIS</span></span>
<span data-ttu-id="481e5-103">Exclui o conjunto de dados de referência com o nome especificado na assinatura especificada, grupo de recursos e ambiente</span><span class="sxs-lookup"><span data-stu-id="481e5-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="481e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="481e5-104">SYNTAX</span></span>

### <span data-ttu-id="481e5-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="481e5-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="481e5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="481e5-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="481e5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="481e5-107">DESCRIPTION</span></span>
<span data-ttu-id="481e5-108">Exclui o conjunto de dados de referência com o nome especificado na assinatura especificada, grupo de recursos e ambiente</span><span class="sxs-lookup"><span data-stu-id="481e5-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="481e5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="481e5-109">EXAMPLES</span></span>

### <span data-ttu-id="481e5-110">Exemplo 1: remover um conjunto de dados de referência especificado por nome</span><span class="sxs-lookup"><span data-stu-id="481e5-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="481e5-111">Esse comando Remove um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="481e5-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="481e5-112">Exemplo 2: remover um conjunto de dados de referência especificado por objeto</span><span class="sxs-lookup"><span data-stu-id="481e5-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="481e5-113">Esse comando Remove um conjunto de dados de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="481e5-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="481e5-114">OS</span><span class="sxs-lookup"><span data-stu-id="481e5-114">PARAMETERS</span></span>

### <span data-ttu-id="481e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481e5-115">-DefaultProfile</span></span>
<span data-ttu-id="481e5-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="481e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="481e5-117">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="481e5-117">-EnvironmentName</span></span>
<span data-ttu-id="481e5-118">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="481e5-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="481e5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="481e5-119">-InputObject</span></span>
<span data-ttu-id="481e5-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="481e5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="481e5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="481e5-121">-Name</span></span>
<span data-ttu-id="481e5-122">O nome do conjunto de dados de referência de série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="481e5-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481e5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="481e5-123">-PassThru</span></span>
<span data-ttu-id="481e5-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="481e5-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="481e5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="481e5-125">-ResourceGroupName</span></span>
<span data-ttu-id="481e5-126">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="481e5-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="481e5-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="481e5-127">-SubscriptionId</span></span>
<span data-ttu-id="481e5-128">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="481e5-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481e5-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="481e5-129">-Confirm</span></span>
<span data-ttu-id="481e5-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="481e5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="481e5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="481e5-131">-WhatIf</span></span>
<span data-ttu-id="481e5-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="481e5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="481e5-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="481e5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="481e5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481e5-134">CommonParameters</span></span>
<span data-ttu-id="481e5-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="481e5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481e5-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="481e5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481e5-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="481e5-137">INPUTS</span></span>

### <span data-ttu-id="481e5-138">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="481e5-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="481e5-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="481e5-139">OUTPUTS</span></span>

### <span data-ttu-id="481e5-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="481e5-140">System.Boolean</span></span>

## <span data-ttu-id="481e5-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="481e5-141">NOTES</span></span>

<span data-ttu-id="481e5-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="481e5-142">ALIASES</span></span>

<span data-ttu-id="481e5-143">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="481e5-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="481e5-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="481e5-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="481e5-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="481e5-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="481e5-146">INPUTobject <ITimeSeriesInsightsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="481e5-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="481e5-147">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="481e5-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="481e5-148">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="481e5-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="481e5-149">`[EventSourceName <String>]`: O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="481e5-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="481e5-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="481e5-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="481e5-151">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="481e5-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="481e5-152">`[ResourceGroupName <String>]`: Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="481e5-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="481e5-153">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="481e5-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="481e5-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="481e5-154">RELATED LINKS</span></span>

