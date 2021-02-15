---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 8ed57766ba36607503994d331cec5381d9f43bbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114979"
---
# <span data-ttu-id="d07c1-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="d07c1-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="d07c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d07c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d07c1-103">Obtém detalhes dos eventos de Recuperação de Site do Azure no cofre.</span><span class="sxs-lookup"><span data-stu-id="d07c1-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="d07c1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d07c1-104">SYNTAX</span></span>

### <span data-ttu-id="d07c1-105">ByParam (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d07c1-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d07c1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d07c1-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d07c1-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="d07c1-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d07c1-108">ByName</span><span class="sxs-lookup"><span data-stu-id="d07c1-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d07c1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d07c1-109">DESCRIPTION</span></span>
<span data-ttu-id="d07c1-110">O **Get-AzRecoveryServicesAsrEvent obtém** a lista de eventos no cofre com base nos filtros de seleção especificados.</span><span class="sxs-lookup"><span data-stu-id="d07c1-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="d07c1-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d07c1-111">EXAMPLES</span></span>

### <span data-ttu-id="d07c1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d07c1-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="d07c1-113">Lista de todos os eventos.</span><span class="sxs-lookup"><span data-stu-id="d07c1-113">List of all events.</span></span>

### <span data-ttu-id="d07c1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d07c1-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="d07c1-115">Obter evento por nome.</span><span class="sxs-lookup"><span data-stu-id="d07c1-115">Get event by name.</span></span>

### <span data-ttu-id="d07c1-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d07c1-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="d07c1-117">Lista de eventos do Objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="d07c1-117">List of event for affected Object.</span></span>

### <span data-ttu-id="d07c1-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="d07c1-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="d07c1-119">Lista de eventos entre a hora de início e a hora de término, gravidade crítica e tipo de saúde VmHealth.</span><span class="sxs-lookup"><span data-stu-id="d07c1-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="d07c1-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d07c1-120">PARAMETERS</span></span>

### <span data-ttu-id="d07c1-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d07c1-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="d07c1-122">Especifica AffectedObject FriendlyName para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d07c1-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07c1-123">-DefaultProfile</span></span>
<span data-ttu-id="d07c1-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d07c1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d07c1-125">-EndTime</span></span>
<span data-ttu-id="d07c1-126">Especifica a hora de término da janela de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d07c1-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="d07c1-127">Use este parâmetro para obter somente os eventos que ocorreram antes do horário especificado.</span><span class="sxs-lookup"><span data-stu-id="d07c1-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="d07c1-128">-EventType</span></span>
<span data-ttu-id="d07c1-129">Filtre eventos pelo tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="d07c1-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-130">-Malha</span><span class="sxs-lookup"><span data-stu-id="d07c1-130">-Fabric</span></span>
<span data-ttu-id="d07c1-131">Filtre eventos pela malha especificada.</span><span class="sxs-lookup"><span data-stu-id="d07c1-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="d07c1-132">-FabricId</span></span>
<span data-ttu-id="d07c1-133">Especifica a ID de fábrica a ser filtrada.</span><span class="sxs-lookup"><span data-stu-id="d07c1-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="d07c1-134">-Name</span></span>
<span data-ttu-id="d07c1-135">Especifica o nome do evento para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d07c1-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d07c1-136">-ResourceId</span></span>
<span data-ttu-id="d07c1-137">Especifica o evento ResourceId do evento.</span><span class="sxs-lookup"><span data-stu-id="d07c1-137">Specifies the event ResourceId of event.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-138">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="d07c1-138">-Severity</span></span>
<span data-ttu-id="d07c1-139">Gravidade do evento para filtrar.</span><span class="sxs-lookup"><span data-stu-id="d07c1-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d07c1-140">-StartTime</span></span>
<span data-ttu-id="d07c1-141">Especifica a hora de início da janela de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d07c1-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="d07c1-142">Use este parâmetro para obter somente os eventos que ocorreram após o tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d07c1-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07c1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07c1-143">CommonParameters</span></span>
<span data-ttu-id="d07c1-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d07c1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07c1-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d07c1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07c1-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="d07c1-146">INPUTS</span></span>

### <span data-ttu-id="d07c1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="d07c1-147">System.String</span></span>

## <span data-ttu-id="d07c1-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="d07c1-148">OUTPUTS</span></span>

### <span data-ttu-id="d07c1-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span><span class="sxs-lookup"><span data-stu-id="d07c1-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="d07c1-150">Notas</span><span class="sxs-lookup"><span data-stu-id="d07c1-150">NOTES</span></span>

## <span data-ttu-id="d07c1-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d07c1-151">RELATED LINKS</span></span>
