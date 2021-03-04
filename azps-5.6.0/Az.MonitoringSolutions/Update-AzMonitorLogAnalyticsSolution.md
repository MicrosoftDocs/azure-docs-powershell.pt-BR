---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: e1c1181dc81d5d15fbaed02fa255961cefe2ae28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889446"
---
# <span data-ttu-id="b2d96-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="b2d96-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="b2d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d96-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d96-103">Atualize as marcas de uma solução.</span><span class="sxs-lookup"><span data-stu-id="b2d96-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="b2d96-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b2d96-104">SYNTAX</span></span>

### <span data-ttu-id="b2d96-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b2d96-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b2d96-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b2d96-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2d96-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b2d96-107">DESCRIPTION</span></span>
<span data-ttu-id="b2d96-108">Atualize as marcas de uma solução.</span><span class="sxs-lookup"><span data-stu-id="b2d96-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="b2d96-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2d96-109">EXAMPLES</span></span>

### <span data-ttu-id="b2d96-110">Exemplo 1: Atualizar uma solução de análise de log de monitoramento pelo nome</span><span class="sxs-lookup"><span data-stu-id="b2d96-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="b2d96-111">Este comando atualiza uma solução de análise de log de monitoramento pelo nome.</span><span class="sxs-lookup"><span data-stu-id="b2d96-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="b2d96-112">Exemplo 2: atualizar uma solução de análise de log de monitoramento por objeto</span><span class="sxs-lookup"><span data-stu-id="b2d96-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="b2d96-113">Este comando atualiza uma solução de análise de log de monitoramento por objeto.</span><span class="sxs-lookup"><span data-stu-id="b2d96-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="b2d96-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b2d96-114">PARAMETERS</span></span>

### <span data-ttu-id="b2d96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d96-115">-DefaultProfile</span></span>
<span data-ttu-id="b2d96-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2d96-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2d96-117">-InputObject</span></span>
<span data-ttu-id="b2d96-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b2d96-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d96-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b2d96-119">-Name</span></span>
<span data-ttu-id="b2d96-120">Nome da Solução de Usuário.</span><span class="sxs-lookup"><span data-stu-id="b2d96-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d96-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d96-121">-ResourceGroupName</span></span>
<span data-ttu-id="b2d96-122">O nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="b2d96-122">The name of the resource group to get.</span></span>
<span data-ttu-id="b2d96-123">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b2d96-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b2d96-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2d96-124">-SubscriptionId</span></span>
<span data-ttu-id="b2d96-125">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d96-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b2d96-126">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b2d96-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b2d96-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2d96-127">-Tag</span></span>
<span data-ttu-id="b2d96-128">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="b2d96-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d96-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2d96-129">-Confirm</span></span>
<span data-ttu-id="b2d96-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2d96-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d96-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d96-131">-WhatIf</span></span>
<span data-ttu-id="b2d96-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2d96-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2d96-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2d96-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d96-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d96-134">CommonParameters</span></span>
<span data-ttu-id="b2d96-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2d96-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d96-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2d96-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d96-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2d96-137">INPUTS</span></span>

### <span data-ttu-id="b2d96-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="b2d96-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="b2d96-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b2d96-139">OUTPUTS</span></span>

### <span data-ttu-id="b2d96-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="b2d96-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="b2d96-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="b2d96-141">NOTES</span></span>

<span data-ttu-id="b2d96-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b2d96-142">ALIASES</span></span>

<span data-ttu-id="b2d96-143">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="b2d96-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2d96-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b2d96-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2d96-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2d96-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2d96-146">INPUTOBJECT <IMonitoringSolutionsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="b2d96-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b2d96-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b2d96-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2d96-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="b2d96-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="b2d96-149">`[ManagementConfigurationName <String>]`: Nome da Configuração de Gerenciamento de Usuário.</span><span class="sxs-lookup"><span data-stu-id="b2d96-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="b2d96-150">`[ProviderName <String>]`: Nome do provedor para o recurso pai.</span><span class="sxs-lookup"><span data-stu-id="b2d96-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="b2d96-151">`[ResourceGroupName <String>]`: O nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="b2d96-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="b2d96-152">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b2d96-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="b2d96-153">`[ResourceName <String>]`: Nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="b2d96-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="b2d96-154">`[ResourceType <String>]`: Tipo de recurso para o recurso pai</span><span class="sxs-lookup"><span data-stu-id="b2d96-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="b2d96-155">`[SolutionName <String>]`: Nome da Solução de Usuário.</span><span class="sxs-lookup"><span data-stu-id="b2d96-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="b2d96-156">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b2d96-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b2d96-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b2d96-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b2d96-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2d96-158">RELATED LINKS</span></span>

