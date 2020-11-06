---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432426"
---
# <span data-ttu-id="c2a69-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="c2a69-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="c2a69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2a69-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a69-103">Obtém detalhes dos eventos do Azure site Recovery no cofre.</span><span class="sxs-lookup"><span data-stu-id="c2a69-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2a69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2a69-104">SYNTAX</span></span>

### <span data-ttu-id="c2a69-105">ByParam (padrão)</span><span class="sxs-lookup"><span data-stu-id="c2a69-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a69-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2a69-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2a69-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="c2a69-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a69-108">ByName</span><span class="sxs-lookup"><span data-stu-id="c2a69-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2a69-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2a69-109">DESCRIPTION</span></span>
<span data-ttu-id="c2a69-110">**Get-AzureRmRecoveryServicesAsrEvent** Obtém a lista de eventos no cofre com base nos filtros de seleção especificados.</span><span class="sxs-lookup"><span data-stu-id="c2a69-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="c2a69-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2a69-111">EXAMPLES</span></span>

### <span data-ttu-id="c2a69-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2a69-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="c2a69-113">Lista de todos os eventos.</span><span class="sxs-lookup"><span data-stu-id="c2a69-113">List of all events.</span></span>

### <span data-ttu-id="c2a69-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c2a69-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


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

<span data-ttu-id="c2a69-115">Obter evento por nome.</span><span class="sxs-lookup"><span data-stu-id="c2a69-115">Get event by name.</span></span>

### <span data-ttu-id="c2a69-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c2a69-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="c2a69-117">Lista de eventos para objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="c2a69-117">List of event for affected Object.</span></span>

### <span data-ttu-id="c2a69-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="c2a69-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="c2a69-119">Lista de eventos entre hora de início e hora de término, gravidade crítica e tipo de integridade VmHealth.</span><span class="sxs-lookup"><span data-stu-id="c2a69-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="c2a69-120">OS</span><span class="sxs-lookup"><span data-stu-id="c2a69-120">PARAMETERS</span></span>

### <span data-ttu-id="c2a69-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c2a69-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="c2a69-122">Especifica FriendlyName afetado para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c2a69-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a69-123">-DefaultProfile</span></span>
<span data-ttu-id="c2a69-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a69-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c2a69-125">-EndTime</span></span>
<span data-ttu-id="c2a69-126">Especifica a hora de término da janela de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c2a69-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="c2a69-127">Use esse parâmetro para obter apenas os eventos que ocorreram antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="c2a69-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="c2a69-128">-EventType</span></span>
<span data-ttu-id="c2a69-129">Filtrar eventos pelo tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="c2a69-129">Filter events by the event type.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="c2a69-130">-Fabric</span></span>
<span data-ttu-id="c2a69-131">Filtrar eventos pela malha especificada.</span><span class="sxs-lookup"><span data-stu-id="c2a69-131">Filter events by the specified fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-132">-Fabricid</span><span class="sxs-lookup"><span data-stu-id="c2a69-132">-FabricId</span></span>
<span data-ttu-id="c2a69-133">Especifica o fabricid para filtrar.</span><span class="sxs-lookup"><span data-stu-id="c2a69-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2a69-134">-Name</span></span>
<span data-ttu-id="c2a69-135">Especifica o nome do evento para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c2a69-135">Specifies name of the event for search.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2a69-136">-ResourceId</span></span>
<span data-ttu-id="c2a69-137">Especifica o evento ReourceId do evento.</span><span class="sxs-lookup"><span data-stu-id="c2a69-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-138">-Severidade</span><span class="sxs-lookup"><span data-stu-id="c2a69-138">-Severity</span></span>
<span data-ttu-id="c2a69-139">Severidade do evento para filtrar.</span><span class="sxs-lookup"><span data-stu-id="c2a69-139">Event severity to filter on.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c2a69-140">-StartTime</span></span>
<span data-ttu-id="c2a69-141">Especifica a hora de início da janela de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c2a69-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="c2a69-142">Use esse parâmetro para obter apenas os eventos que ocorreram após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="c2a69-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a69-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a69-143">CommonParameters</span></span>
<span data-ttu-id="c2a69-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a69-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a69-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2a69-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a69-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2a69-146">INPUTS</span></span>

### <span data-ttu-id="c2a69-147">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c2a69-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c2a69-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2a69-148">OUTPUTS</span></span>

### <span data-ttu-id="c2a69-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASREvent, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c2a69-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c2a69-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2a69-150">NOTES</span></span>

## <span data-ttu-id="c2a69-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2a69-151">RELATED LINKS</span></span>
