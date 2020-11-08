---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125343"
---
# <span data-ttu-id="76c56-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="76c56-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="76c56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76c56-102">SYNOPSIS</span></span>
<span data-ttu-id="76c56-103">Exclui a solução na assinatura.</span><span class="sxs-lookup"><span data-stu-id="76c56-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="76c56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76c56-104">SYNTAX</span></span>

### <span data-ttu-id="76c56-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="76c56-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76c56-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76c56-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76c56-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76c56-107">DESCRIPTION</span></span>
<span data-ttu-id="76c56-108">Exclui a solução na assinatura.</span><span class="sxs-lookup"><span data-stu-id="76c56-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="76c56-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76c56-109">EXAMPLES</span></span>

### <span data-ttu-id="76c56-110">Exemplo 1: remover uma solução de análise de logs de monitor por nome</span><span class="sxs-lookup"><span data-stu-id="76c56-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="76c56-111">Esse comando Remove uma solução de análise de log de monitor por nome.</span><span class="sxs-lookup"><span data-stu-id="76c56-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="76c56-112">Exemplo 2: remover uma solução de análise de logs de monitor por objeto</span><span class="sxs-lookup"><span data-stu-id="76c56-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="76c56-113">Esse comando Remove uma solução de análise de log de monitor por objeto.</span><span class="sxs-lookup"><span data-stu-id="76c56-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="76c56-114">Exemplo 3: remover uma solução de análise de logs de monitor por pipeline</span><span class="sxs-lookup"><span data-stu-id="76c56-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="76c56-115">Esse comando Remove uma solução de análise de log de monitor por pipeline.</span><span class="sxs-lookup"><span data-stu-id="76c56-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="76c56-116">OS</span><span class="sxs-lookup"><span data-stu-id="76c56-116">PARAMETERS</span></span>

### <span data-ttu-id="76c56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c56-117">-DefaultProfile</span></span>
<span data-ttu-id="76c56-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76c56-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c56-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76c56-119">-InputObject</span></span>
<span data-ttu-id="76c56-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="76c56-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="76c56-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="76c56-121">-Name</span></span>
<span data-ttu-id="76c56-122">Nome da solução de usuário.</span><span class="sxs-lookup"><span data-stu-id="76c56-122">User Solution Name.</span></span>

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

### <span data-ttu-id="76c56-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76c56-123">-PassThru</span></span>
<span data-ttu-id="76c56-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="76c56-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="76c56-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c56-125">-ResourceGroupName</span></span>
<span data-ttu-id="76c56-126">O nome do grupo de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="76c56-126">The name of the resource group to get.</span></span>
<span data-ttu-id="76c56-127">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="76c56-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="76c56-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76c56-128">-SubscriptionId</span></span>
<span data-ttu-id="76c56-129">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="76c56-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76c56-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="76c56-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="76c56-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76c56-131">-Confirm</span></span>
<span data-ttu-id="76c56-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76c56-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c56-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c56-133">-WhatIf</span></span>
<span data-ttu-id="76c56-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76c56-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c56-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76c56-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c56-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c56-136">CommonParameters</span></span>
<span data-ttu-id="76c56-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c56-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c56-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76c56-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c56-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76c56-139">INPUTS</span></span>

### <span data-ttu-id="76c56-140">Microsoft. Azure. PowerShell. cmdlets. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="76c56-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="76c56-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76c56-141">OUTPUTS</span></span>

### <span data-ttu-id="76c56-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76c56-142">System.Boolean</span></span>

## <span data-ttu-id="76c56-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76c56-143">NOTES</span></span>

<span data-ttu-id="76c56-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="76c56-144">ALIASES</span></span>

<span data-ttu-id="76c56-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="76c56-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76c56-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="76c56-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76c56-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76c56-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76c56-148">INPUTobject <IMonitoringSolutionsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="76c56-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76c56-149">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="76c56-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76c56-150">`[ManagementAssociationName <String>]`: Nome do ManagementAssociation do usuário.</span><span class="sxs-lookup"><span data-stu-id="76c56-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="76c56-151">`[ManagementConfigurationName <String>]`: Nome de configuração de gerenciamento de usuários.</span><span class="sxs-lookup"><span data-stu-id="76c56-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="76c56-152">`[ProviderName <String>]`: Nome do provedor para o recurso pai.</span><span class="sxs-lookup"><span data-stu-id="76c56-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="76c56-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="76c56-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="76c56-154">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="76c56-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="76c56-155">`[ResourceName <String>]`: Nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="76c56-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="76c56-156">`[ResourceType <String>]`: Tipo de recurso do recurso pai</span><span class="sxs-lookup"><span data-stu-id="76c56-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="76c56-157">`[SolutionName <String>]`: Nome da solução de usuário.</span><span class="sxs-lookup"><span data-stu-id="76c56-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="76c56-158">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="76c56-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="76c56-159">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="76c56-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="76c56-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76c56-160">RELATED LINKS</span></span>

