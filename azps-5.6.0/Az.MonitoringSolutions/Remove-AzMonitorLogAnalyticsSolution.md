---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: f3a41317663c5b1009a45bfe711cdf3410a784c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889450"
---
# <span data-ttu-id="9f166-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="9f166-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="9f166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f166-102">SYNOPSIS</span></span>
<span data-ttu-id="9f166-103">Exclui a solução na assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f166-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="9f166-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9f166-104">SYNTAX</span></span>

### <span data-ttu-id="9f166-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9f166-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9f166-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f166-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f166-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9f166-107">DESCRIPTION</span></span>
<span data-ttu-id="9f166-108">Exclui a solução na assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f166-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="9f166-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f166-109">EXAMPLES</span></span>

### <span data-ttu-id="9f166-110">Exemplo 1: Remover uma solução de análise de log de monitoramento pelo nome</span><span class="sxs-lookup"><span data-stu-id="9f166-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="9f166-111">Este comando remove uma solução de análise de log de monitoramento pelo nome.</span><span class="sxs-lookup"><span data-stu-id="9f166-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="9f166-112">Exemplo 2: Remover uma solução de análise de log de monitoramento por objeto</span><span class="sxs-lookup"><span data-stu-id="9f166-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="9f166-113">Este comando remove uma solução de análise de log de monitoramento por objeto.</span><span class="sxs-lookup"><span data-stu-id="9f166-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="9f166-114">Exemplo 3: Remover uma solução de análise de log de monitoramento por pipeline</span><span class="sxs-lookup"><span data-stu-id="9f166-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="9f166-115">Este comando remove uma solução de análise de log de monitoramento por pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f166-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="9f166-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9f166-116">PARAMETERS</span></span>

### <span data-ttu-id="9f166-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f166-117">-DefaultProfile</span></span>
<span data-ttu-id="9f166-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f166-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f166-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f166-119">-InputObject</span></span>
<span data-ttu-id="9f166-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9f166-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f166-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9f166-121">-Name</span></span>
<span data-ttu-id="9f166-122">Nome da Solução de Usuário.</span><span class="sxs-lookup"><span data-stu-id="9f166-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f166-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f166-123">-PassThru</span></span>
<span data-ttu-id="9f166-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="9f166-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9f166-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f166-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f166-126">O nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="9f166-126">The name of the resource group to get.</span></span>
<span data-ttu-id="9f166-127">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9f166-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9f166-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f166-128">-SubscriptionId</span></span>
<span data-ttu-id="9f166-129">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f166-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9f166-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9f166-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9f166-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f166-131">-Confirm</span></span>
<span data-ttu-id="9f166-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f166-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f166-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f166-133">-WhatIf</span></span>
<span data-ttu-id="9f166-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f166-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f166-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f166-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f166-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f166-136">CommonParameters</span></span>
<span data-ttu-id="9f166-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f166-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f166-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f166-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f166-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f166-139">INPUTS</span></span>

### <span data-ttu-id="9f166-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="9f166-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="9f166-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9f166-141">OUTPUTS</span></span>

### <span data-ttu-id="9f166-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f166-142">System.Boolean</span></span>

## <span data-ttu-id="9f166-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="9f166-143">NOTES</span></span>

<span data-ttu-id="9f166-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9f166-144">ALIASES</span></span>

<span data-ttu-id="9f166-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="9f166-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f166-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9f166-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f166-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f166-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f166-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="9f166-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9f166-149">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9f166-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f166-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="9f166-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="9f166-151">`[ManagementConfigurationName <String>]`: Nome da Configuração de Gerenciamento de Usuário.</span><span class="sxs-lookup"><span data-stu-id="9f166-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="9f166-152">`[ProviderName <String>]`: Nome do provedor para o recurso pai.</span><span class="sxs-lookup"><span data-stu-id="9f166-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="9f166-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="9f166-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="9f166-154">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9f166-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="9f166-155">`[ResourceName <String>]`: Nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="9f166-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="9f166-156">`[ResourceType <String>]`: Tipo de recurso para o recurso pai</span><span class="sxs-lookup"><span data-stu-id="9f166-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="9f166-157">`[SolutionName <String>]`: Nome da Solução de Usuário.</span><span class="sxs-lookup"><span data-stu-id="9f166-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="9f166-158">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f166-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9f166-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9f166-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9f166-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f166-160">RELATED LINKS</span></span>

