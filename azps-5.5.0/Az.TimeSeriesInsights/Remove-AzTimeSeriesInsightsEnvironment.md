---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114351"
---
# <span data-ttu-id="19981-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="19981-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="19981-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19981-102">SYNOPSIS</span></span>
<span data-ttu-id="19981-103">Exclui o ambiente com o nome especificado no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="19981-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="19981-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19981-104">SYNTAX</span></span>

### <span data-ttu-id="19981-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="19981-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="19981-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19981-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="19981-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="19981-107">DESCRIPTION</span></span>
<span data-ttu-id="19981-108">Exclui o ambiente com o nome especificado no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="19981-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="19981-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="19981-109">EXAMPLES</span></span>

### <span data-ttu-id="19981-110">Exemplo 1: remover um ambiente de insights de série de tempo por nome</span><span class="sxs-lookup"><span data-stu-id="19981-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="19981-111">Esse comando remove um ambiente de informações de séries temportivas.</span><span class="sxs-lookup"><span data-stu-id="19981-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="19981-112">Exemplo 2: Remover um ambiente de insights de série de tempo por objeto</span><span class="sxs-lookup"><span data-stu-id="19981-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="19981-113">Esse comando remove um ambiente de informações de séries temportivas.</span><span class="sxs-lookup"><span data-stu-id="19981-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="19981-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19981-114">PARAMETERS</span></span>

### <span data-ttu-id="19981-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19981-115">-DefaultProfile</span></span>
<span data-ttu-id="19981-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19981-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19981-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19981-117">-InputObject</span></span>
<span data-ttu-id="19981-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="19981-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="19981-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="19981-119">-Name</span></span>
<span data-ttu-id="19981-120">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="19981-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19981-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19981-121">-PassThru</span></span>
<span data-ttu-id="19981-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="19981-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="19981-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19981-123">-ResourceGroupName</span></span>
<span data-ttu-id="19981-124">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="19981-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="19981-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19981-125">-SubscriptionId</span></span>
<span data-ttu-id="19981-126">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="19981-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="19981-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="19981-127">-Confirm</span></span>
<span data-ttu-id="19981-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19981-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19981-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19981-129">-WhatIf</span></span>
<span data-ttu-id="19981-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="19981-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19981-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19981-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19981-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19981-132">CommonParameters</span></span>
<span data-ttu-id="19981-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19981-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19981-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19981-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19981-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="19981-135">INPUTS</span></span>

### <span data-ttu-id="19981-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="19981-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="19981-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="19981-137">OUTPUTS</span></span>

### <span data-ttu-id="19981-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19981-138">System.Boolean</span></span>

## <span data-ttu-id="19981-139">Notas</span><span class="sxs-lookup"><span data-stu-id="19981-139">NOTES</span></span>

<span data-ttu-id="19981-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="19981-140">ALIASES</span></span>

<span data-ttu-id="19981-141">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="19981-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19981-142">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="19981-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19981-143">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19981-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19981-144">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="19981-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19981-145">`[AccessPolicyName <String>]`: nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="19981-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="19981-146">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="19981-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="19981-147">`[EventSourceName <String>]`: o nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="19981-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="19981-148">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="19981-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19981-149">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="19981-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="19981-150">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="19981-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="19981-151">`[SubscriptionId <String>]`: ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="19981-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="19981-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19981-152">RELATED LINKS</span></span>

