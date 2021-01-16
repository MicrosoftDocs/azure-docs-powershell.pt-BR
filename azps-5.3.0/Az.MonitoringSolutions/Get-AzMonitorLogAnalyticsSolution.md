---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428608"
---
# <span data-ttu-id="30489-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="30489-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="30489-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30489-102">SYNOPSIS</span></span>
<span data-ttu-id="30489-103">Recupera a solução de usuário.</span><span class="sxs-lookup"><span data-stu-id="30489-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="30489-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30489-104">SYNTAX</span></span>

### <span data-ttu-id="30489-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="30489-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="30489-106">Obter</span><span class="sxs-lookup"><span data-stu-id="30489-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="30489-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="30489-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="30489-108">Programação</span><span class="sxs-lookup"><span data-stu-id="30489-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="30489-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30489-109">DESCRIPTION</span></span>
<span data-ttu-id="30489-110">Recupera a solução de usuário.</span><span class="sxs-lookup"><span data-stu-id="30489-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="30489-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30489-111">EXAMPLES</span></span>

### <span data-ttu-id="30489-112">Exemplo 1: obter uma solução de análise de logs de monitor por nome</span><span class="sxs-lookup"><span data-stu-id="30489-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="30489-113">Esse comando obtém uma solução de análise de logs de monitor por nome.</span><span class="sxs-lookup"><span data-stu-id="30489-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="30489-114">Exemplo 2: obter uma solução de análise de log de monitor por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="30489-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="30489-115">Este comando obtém uma solução de análise de logs de monitor por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="30489-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="30489-116">Exemplo 3: obter uma solução de análise de logs de monitor por objeto</span><span class="sxs-lookup"><span data-stu-id="30489-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="30489-117">Esse comando obtém uma solução de análise de logs de monitor por objeto.</span><span class="sxs-lookup"><span data-stu-id="30489-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="30489-118">Exemplo 4: obter todas as soluções de análise de logs de monitor em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="30489-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="30489-119">Esse comando obtém todas as soluções de análise de logs de monitor em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="30489-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="30489-120">Exemplo 5: obter todas as soluções de análise de log de monitor em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="30489-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="30489-121">Este comando obtém todas as soluções de análise de logs de monitor em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="30489-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="30489-122">OS</span><span class="sxs-lookup"><span data-stu-id="30489-122">PARAMETERS</span></span>

### <span data-ttu-id="30489-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30489-123">-DefaultProfile</span></span>
<span data-ttu-id="30489-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30489-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30489-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30489-125">-InputObject</span></span>
<span data-ttu-id="30489-126">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="30489-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="30489-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="30489-127">-Name</span></span>
<span data-ttu-id="30489-128">Nome da solução de usuário.</span><span class="sxs-lookup"><span data-stu-id="30489-128">User Solution Name.</span></span>

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

### <span data-ttu-id="30489-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30489-129">-ResourceGroupName</span></span>
<span data-ttu-id="30489-130">O nome do grupo de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="30489-130">The name of the resource group to get.</span></span>
<span data-ttu-id="30489-131">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="30489-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="30489-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30489-132">-SubscriptionId</span></span>
<span data-ttu-id="30489-133">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="30489-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="30489-134">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="30489-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="30489-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30489-135">CommonParameters</span></span>
<span data-ttu-id="30489-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30489-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30489-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30489-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30489-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30489-138">INPUTS</span></span>

### <span data-ttu-id="30489-139">Microsoft. Azure. PowerShell. cmdlets. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="30489-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="30489-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30489-140">OUTPUTS</span></span>

### <span data-ttu-id="30489-141">Microsoft. Azure. PowerShell. cmdlets. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="30489-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="30489-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30489-142">NOTES</span></span>

<span data-ttu-id="30489-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="30489-143">ALIASES</span></span>

<span data-ttu-id="30489-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="30489-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30489-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="30489-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30489-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30489-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30489-147">INPUTobject <IMonitoringSolutionsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="30489-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30489-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="30489-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30489-149">`[ManagementAssociationName <String>]`: Nome do ManagementAssociation do usuário.</span><span class="sxs-lookup"><span data-stu-id="30489-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="30489-150">`[ManagementConfigurationName <String>]`: Nome de configuração de gerenciamento de usuários.</span><span class="sxs-lookup"><span data-stu-id="30489-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="30489-151">`[ProviderName <String>]`: Nome do provedor para o recurso pai.</span><span class="sxs-lookup"><span data-stu-id="30489-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="30489-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="30489-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="30489-153">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="30489-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="30489-154">`[ResourceName <String>]`: Nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="30489-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="30489-155">`[ResourceType <String>]`: Tipo de recurso do recurso pai</span><span class="sxs-lookup"><span data-stu-id="30489-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="30489-156">`[SolutionName <String>]`: Nome da solução de usuário.</span><span class="sxs-lookup"><span data-stu-id="30489-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="30489-157">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="30489-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="30489-158">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="30489-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="30489-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30489-159">RELATED LINKS</span></span>

