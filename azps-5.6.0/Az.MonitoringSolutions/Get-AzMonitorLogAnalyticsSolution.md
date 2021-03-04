---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: f4be2a5da2dc8455b6e6674e7e74050ea506ae0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889451"
---
# <span data-ttu-id="9e5fd-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="9e5fd-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="9e5fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e5fd-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5fd-103">Recupera a solução do usuário.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="9e5fd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9e5fd-104">SYNTAX</span></span>

### <span data-ttu-id="9e5fd-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9e5fd-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e5fd-106">Obter</span><span class="sxs-lookup"><span data-stu-id="9e5fd-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e5fd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9e5fd-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e5fd-108">Listar</span><span class="sxs-lookup"><span data-stu-id="9e5fd-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9e5fd-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9e5fd-109">DESCRIPTION</span></span>
<span data-ttu-id="9e5fd-110">Recupera a solução do usuário.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="9e5fd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e5fd-111">EXAMPLES</span></span>

### <span data-ttu-id="9e5fd-112">Exemplo 1: obter uma solução de análise de log de monitoramento pelo nome</span><span class="sxs-lookup"><span data-stu-id="9e5fd-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="9e5fd-113">Este comando obtém uma solução de análise de log de monitoramento pelo nome.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="9e5fd-114">Exemplo 2: Obter uma solução de análise de log de monitoramento por id de recurso</span><span class="sxs-lookup"><span data-stu-id="9e5fd-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="9e5fd-115">Este comando obtém uma solução de análise de log de monitoramento por id de recurso.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="9e5fd-116">Exemplo 3: Obter uma solução de análise de log de monitoramento por objeto</span><span class="sxs-lookup"><span data-stu-id="9e5fd-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="9e5fd-117">Este comando obtém uma solução de análise de log de monitoramento por objeto.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="9e5fd-118">Exemplo 4: Obter todas as soluções de análise de log de monitoramento em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9e5fd-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="9e5fd-119">Este comando obtém todas as soluções de análise de log de monitoramento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="9e5fd-120">Exemplo 5: Obter todas as soluções de análise de log de monitoramento em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="9e5fd-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="9e5fd-121">Este comando obtém todas as soluções de análise de log de monitoramento em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="9e5fd-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9e5fd-122">PARAMETERS</span></span>

### <span data-ttu-id="9e5fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5fd-123">-DefaultProfile</span></span>
<span data-ttu-id="9e5fd-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e5fd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e5fd-125">-InputObject</span></span>
<span data-ttu-id="9e5fd-126">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e5fd-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9e5fd-127">-Name</span></span>
<span data-ttu-id="9e5fd-128">Nome da Solução de Usuário.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e5fd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e5fd-129">-ResourceGroupName</span></span>
<span data-ttu-id="9e5fd-130">O nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-130">The name of the resource group to get.</span></span>
<span data-ttu-id="9e5fd-131">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9e5fd-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e5fd-132">-SubscriptionId</span></span>
<span data-ttu-id="9e5fd-133">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9e5fd-134">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e5fd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5fd-135">CommonParameters</span></span>
<span data-ttu-id="9e5fd-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5fd-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e5fd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5fd-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e5fd-138">INPUTS</span></span>

### <span data-ttu-id="9e5fd-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="9e5fd-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="9e5fd-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9e5fd-140">OUTPUTS</span></span>

### <span data-ttu-id="9e5fd-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="9e5fd-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="9e5fd-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="9e5fd-142">NOTES</span></span>

<span data-ttu-id="9e5fd-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9e5fd-143">ALIASES</span></span>

<span data-ttu-id="9e5fd-144">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="9e5fd-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e5fd-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e5fd-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e5fd-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="9e5fd-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e5fd-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9e5fd-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e5fd-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="9e5fd-150">`[ManagementConfigurationName <String>]`: Nome da Configuração de Gerenciamento de Usuário.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="9e5fd-151">`[ProviderName <String>]`: Nome do provedor para o recurso pai.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="9e5fd-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="9e5fd-153">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="9e5fd-154">`[ResourceName <String>]`: Nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="9e5fd-155">`[ResourceType <String>]`: Tipo de recurso para o recurso pai</span><span class="sxs-lookup"><span data-stu-id="9e5fd-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="9e5fd-156">`[SolutionName <String>]`: Nome da Solução de Usuário.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="9e5fd-157">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9e5fd-158">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e5fd-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9e5fd-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e5fd-159">RELATED LINKS</span></span>

