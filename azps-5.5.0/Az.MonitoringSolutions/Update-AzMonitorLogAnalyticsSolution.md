---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112943"
---
# <span data-ttu-id="b7827-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="b7827-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="b7827-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7827-102">SYNOPSIS</span></span>
<span data-ttu-id="b7827-103">Atualize as marcas de uma solução.</span><span class="sxs-lookup"><span data-stu-id="b7827-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="b7827-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7827-104">SYNTAX</span></span>

### <span data-ttu-id="b7827-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b7827-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7827-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b7827-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7827-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7827-107">DESCRIPTION</span></span>
<span data-ttu-id="b7827-108">Atualize as marcas de uma solução.</span><span class="sxs-lookup"><span data-stu-id="b7827-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="b7827-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b7827-109">EXAMPLES</span></span>

### <span data-ttu-id="b7827-110">Exemplo 1: Atualizar uma solução de análise de log de monitor por nome</span><span class="sxs-lookup"><span data-stu-id="b7827-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="b7827-111">Esse comando atualiza uma solução de análise de log de monitor por nome.</span><span class="sxs-lookup"><span data-stu-id="b7827-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="b7827-112">Exemplo 2: Atualizar uma solução de análise de log de monitor por objeto</span><span class="sxs-lookup"><span data-stu-id="b7827-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="b7827-113">Esse comando atualiza uma solução de análise de log de monitor por objeto.</span><span class="sxs-lookup"><span data-stu-id="b7827-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="b7827-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7827-114">PARAMETERS</span></span>

### <span data-ttu-id="b7827-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7827-115">-DefaultProfile</span></span>
<span data-ttu-id="b7827-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7827-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7827-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7827-117">-InputObject</span></span>
<span data-ttu-id="b7827-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="b7827-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7827-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7827-119">-Name</span></span>
<span data-ttu-id="b7827-120">Nome da Solução de Usuário.</span><span class="sxs-lookup"><span data-stu-id="b7827-120">User Solution Name.</span></span>

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

### <span data-ttu-id="b7827-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7827-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7827-122">O nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="b7827-122">The name of the resource group to get.</span></span>
<span data-ttu-id="b7827-123">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b7827-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b7827-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7827-124">-SubscriptionId</span></span>
<span data-ttu-id="b7827-125">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7827-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7827-126">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7827-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b7827-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7827-127">-Tag</span></span>
<span data-ttu-id="b7827-128">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="b7827-128">Resource tags</span></span>

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

### <span data-ttu-id="b7827-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b7827-129">-Confirm</span></span>
<span data-ttu-id="b7827-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7827-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7827-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7827-131">-WhatIf</span></span>
<span data-ttu-id="b7827-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b7827-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7827-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7827-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7827-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7827-134">CommonParameters</span></span>
<span data-ttu-id="b7827-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7827-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7827-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7827-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7827-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="b7827-137">INPUTS</span></span>

### <span data-ttu-id="b7827-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="b7827-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="b7827-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="b7827-139">OUTPUTS</span></span>

### <span data-ttu-id="b7827-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="b7827-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="b7827-141">Notas</span><span class="sxs-lookup"><span data-stu-id="b7827-141">NOTES</span></span>

<span data-ttu-id="b7827-142">Aliases</span><span class="sxs-lookup"><span data-stu-id="b7827-142">ALIASES</span></span>

<span data-ttu-id="b7827-143">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="b7827-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7827-144">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b7827-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7827-145">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7827-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7827-146">INPUTOBJECT: <IMonitoringSolutionsIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="b7827-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7827-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="b7827-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7827-148">`[ManagementAssociationName <String>]`: Nome daSsociação de Gerenciamento de Usuários.</span><span class="sxs-lookup"><span data-stu-id="b7827-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="b7827-149">`[ManagementConfigurationName <String>]`: Nome de configuração de gerenciamento de usuário.</span><span class="sxs-lookup"><span data-stu-id="b7827-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="b7827-150">`[ProviderName <String>]`: Nome do provedor para o recurso pai.</span><span class="sxs-lookup"><span data-stu-id="b7827-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="b7827-151">`[ResourceGroupName <String>]`: o nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="b7827-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="b7827-152">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b7827-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="b7827-153">`[ResourceName <String>]`: nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="b7827-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="b7827-154">`[ResourceType <String>]`: Tipo de recurso para o recurso pai</span><span class="sxs-lookup"><span data-stu-id="b7827-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="b7827-155">`[SolutionName <String>]`: Nome da solução de usuário.</span><span class="sxs-lookup"><span data-stu-id="b7827-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="b7827-156">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7827-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b7827-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7827-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b7827-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7827-158">RELATED LINKS</span></span>

