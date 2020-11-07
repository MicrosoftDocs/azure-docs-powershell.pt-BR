---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 673343029608935c629c6240d1bc1f5ec5a7d4e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773051"
---
# <span data-ttu-id="181f4-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="181f4-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="181f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="181f4-102">SYNOPSIS</span></span>
<span data-ttu-id="181f4-103">Obtém detalhes dos eventos do Azure site Recovery no cofre.</span><span class="sxs-lookup"><span data-stu-id="181f4-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="181f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="181f4-104">SYNTAX</span></span>

### <span data-ttu-id="181f4-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="181f4-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="181f4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="181f4-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="181f4-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="181f4-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="181f4-108">ByName</span><span class="sxs-lookup"><span data-stu-id="181f4-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181f4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="181f4-109">DESCRIPTION</span></span>
<span data-ttu-id="181f4-110">**Get-AzRecoveryServicesAsrEvent** Obtém a lista de eventos no cofre com base nos filtros de seleção especificados.</span><span class="sxs-lookup"><span data-stu-id="181f4-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="181f4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="181f4-111">EXAMPLES</span></span>

### <span data-ttu-id="181f4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="181f4-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="181f4-113">Lista de todos os eventos.</span><span class="sxs-lookup"><span data-stu-id="181f4-113">List of all events.</span></span>

### <span data-ttu-id="181f4-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="181f4-114">Example 2</span></span>
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

<span data-ttu-id="181f4-115">Obter evento por nome.</span><span class="sxs-lookup"><span data-stu-id="181f4-115">Get event by name.</span></span>

### <span data-ttu-id="181f4-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="181f4-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="181f4-117">Lista de eventos para objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="181f4-117">List of event for affected Object.</span></span>

### <span data-ttu-id="181f4-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="181f4-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="181f4-119">Lista de eventos entre hora de início e hora de término, gravidade crítica e tipo de integridade VmHealth.</span><span class="sxs-lookup"><span data-stu-id="181f4-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="181f4-120">OS</span><span class="sxs-lookup"><span data-stu-id="181f4-120">PARAMETERS</span></span>

### <span data-ttu-id="181f4-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="181f4-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="181f4-122">Especifica FriendlyName afetado para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="181f4-122">Specifies AffectedObject FriendlyName for the search.</span></span>

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

### <span data-ttu-id="181f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181f4-123">-DefaultProfile</span></span>
<span data-ttu-id="181f4-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="181f4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="181f4-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="181f4-125">-EndTime</span></span>
<span data-ttu-id="181f4-126">Especifica a hora de término da janela de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="181f4-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="181f4-127">Use esse parâmetro para obter apenas os eventos que ocorreram antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="181f4-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

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

### <span data-ttu-id="181f4-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="181f4-128">-EventType</span></span>
<span data-ttu-id="181f4-129">Filtrar eventos pelo tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="181f4-129">Filter events by the event type.</span></span>

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

### <span data-ttu-id="181f4-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="181f4-130">-Fabric</span></span>
<span data-ttu-id="181f4-131">Filtrar eventos pela malha especificada.</span><span class="sxs-lookup"><span data-stu-id="181f4-131">Filter events by the specified fabric.</span></span>

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

### <span data-ttu-id="181f4-132">-Fabricid</span><span class="sxs-lookup"><span data-stu-id="181f4-132">-FabricId</span></span>
<span data-ttu-id="181f4-133">Especifica o fabricid para filtrar.</span><span class="sxs-lookup"><span data-stu-id="181f4-133">Specifies the fabricId to filter.</span></span>

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

### <span data-ttu-id="181f4-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="181f4-134">-Name</span></span>
<span data-ttu-id="181f4-135">Especifica o nome do evento para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="181f4-135">Specifies name of the event for search.</span></span>

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

### <span data-ttu-id="181f4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="181f4-136">-ResourceId</span></span>
<span data-ttu-id="181f4-137">Especifica o ResourceId do evento.</span><span class="sxs-lookup"><span data-stu-id="181f4-137">Specifies the event ResourceId of event.</span></span>

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

### <span data-ttu-id="181f4-138">-Severidade</span><span class="sxs-lookup"><span data-stu-id="181f4-138">-Severity</span></span>
<span data-ttu-id="181f4-139">Severidade do evento para filtrar.</span><span class="sxs-lookup"><span data-stu-id="181f4-139">Event severity to filter on.</span></span>

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

### <span data-ttu-id="181f4-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="181f4-140">-StartTime</span></span>
<span data-ttu-id="181f4-141">Especifica a hora de início da janela de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="181f4-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="181f4-142">Use esse parâmetro para obter apenas os eventos que ocorreram após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="181f4-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

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

### <span data-ttu-id="181f4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181f4-143">CommonParameters</span></span>
<span data-ttu-id="181f4-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181f4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181f4-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181f4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181f4-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="181f4-146">INPUTS</span></span>

### <span data-ttu-id="181f4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="181f4-147">System.String</span></span>

## <span data-ttu-id="181f4-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="181f4-148">OUTPUTS</span></span>

### <span data-ttu-id="181f4-149">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASREvent</span><span class="sxs-lookup"><span data-stu-id="181f4-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="181f4-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="181f4-150">NOTES</span></span>

## <span data-ttu-id="181f4-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="181f4-151">RELATED LINKS</span></span>
