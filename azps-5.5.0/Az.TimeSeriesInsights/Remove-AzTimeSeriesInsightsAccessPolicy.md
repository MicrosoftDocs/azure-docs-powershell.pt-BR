---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114353"
---
# <span data-ttu-id="4b301-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4b301-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="4b301-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b301-102">SYNOPSIS</span></span>
<span data-ttu-id="4b301-103">Exclui a política de acesso com o nome especificado na assinatura, grupo de recursos e ambiente especificados</span><span class="sxs-lookup"><span data-stu-id="4b301-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="4b301-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b301-104">SYNTAX</span></span>

### <span data-ttu-id="4b301-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4b301-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b301-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4b301-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4b301-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b301-107">DESCRIPTION</span></span>
<span data-ttu-id="4b301-108">Exclui a política de acesso com o nome especificado na assinatura, grupo de recursos e ambiente especificados</span><span class="sxs-lookup"><span data-stu-id="4b301-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="4b301-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b301-109">EXAMPLES</span></span>

### <span data-ttu-id="4b301-110">Exemplo 1: Remover uma política de acesso especificada por nome</span><span class="sxs-lookup"><span data-stu-id="4b301-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="4b301-111">Esse comando remove uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="4b301-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="4b301-112">Exemplo 2: Remover uma política de acesso especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="4b301-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="4b301-113">Esse comando remove uma política de acesso especificada.</span><span class="sxs-lookup"><span data-stu-id="4b301-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="4b301-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b301-114">PARAMETERS</span></span>

### <span data-ttu-id="4b301-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b301-115">-DefaultProfile</span></span>
<span data-ttu-id="4b301-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b301-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b301-117">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="4b301-117">-EnvironmentName</span></span>
<span data-ttu-id="4b301-118">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="4b301-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="4b301-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b301-119">-InputObject</span></span>
<span data-ttu-id="4b301-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4b301-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b301-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b301-121">-Name</span></span>
<span data-ttu-id="4b301-122">O nome da política de acesso Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="4b301-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b301-123">-PassThru</span></span>
<span data-ttu-id="4b301-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="4b301-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4b301-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b301-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b301-126">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b301-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="4b301-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b301-127">-SubscriptionId</span></span>
<span data-ttu-id="4b301-128">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b301-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4b301-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4b301-129">-Confirm</span></span>
<span data-ttu-id="4b301-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b301-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b301-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b301-131">-WhatIf</span></span>
<span data-ttu-id="4b301-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4b301-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b301-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b301-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b301-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b301-134">CommonParameters</span></span>
<span data-ttu-id="4b301-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b301-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b301-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b301-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b301-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b301-137">INPUTS</span></span>

### <span data-ttu-id="4b301-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="4b301-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="4b301-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b301-139">OUTPUTS</span></span>

### <span data-ttu-id="4b301-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b301-140">System.Boolean</span></span>

## <span data-ttu-id="4b301-141">Notas</span><span class="sxs-lookup"><span data-stu-id="4b301-141">NOTES</span></span>

<span data-ttu-id="4b301-142">Aliases</span><span class="sxs-lookup"><span data-stu-id="4b301-142">ALIASES</span></span>

<span data-ttu-id="4b301-143">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4b301-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b301-144">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4b301-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b301-145">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b301-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b301-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="4b301-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b301-147">`[AccessPolicyName <String>]`: nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="4b301-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="4b301-148">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="4b301-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="4b301-149">`[EventSourceName <String>]`: o nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="4b301-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="4b301-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4b301-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b301-151">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="4b301-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="4b301-152">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b301-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="4b301-153">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b301-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="4b301-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b301-154">RELATED LINKS</span></span>

