---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 5f2dfec045364852d9846fa3bb35bd903c78ca5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258435"
---
# <span data-ttu-id="417d3-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="417d3-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="417d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="417d3-102">SYNOPSIS</span></span>
<span data-ttu-id="417d3-103">Obtém as informações sobre as agendas de largura de banda</span><span class="sxs-lookup"><span data-stu-id="417d3-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="417d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="417d3-104">SYNTAX</span></span>

### <span data-ttu-id="417d3-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="417d3-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="417d3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="417d3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="417d3-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="417d3-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="417d3-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="417d3-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="417d3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="417d3-109">DESCRIPTION</span></span>
<span data-ttu-id="417d3-110">O cmdlet **Get-AzStackEdgeBandwidthSchedule** Obtém as informações sobre as agendas de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="417d3-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="417d3-111">Você pode especificar o nome de um cronograma juntamente com o nome do grupo de recursos e o nome do dispositivo para obter as informações sobre um agendamento de largura de banda específico</span><span class="sxs-lookup"><span data-stu-id="417d3-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="417d3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="417d3-112">EXAMPLES</span></span>

### <span data-ttu-id="417d3-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="417d3-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="417d3-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="417d3-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="417d3-115">OS</span><span class="sxs-lookup"><span data-stu-id="417d3-115">PARAMETERS</span></span>

### <span data-ttu-id="417d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417d3-116">-DefaultProfile</span></span>
<span data-ttu-id="417d3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="417d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="417d3-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="417d3-118">-DeviceName</span></span>
<span data-ttu-id="417d3-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="417d3-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417d3-120">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="417d3-120">-DeviceObject</span></span>
<span data-ttu-id="417d3-121">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="417d3-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="417d3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="417d3-122">-Name</span></span>
<span data-ttu-id="417d3-123">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="417d3-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: BandwidthScheduleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="417d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="417d3-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="417d3-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417d3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="417d3-126">-ResourceId</span></span>
<span data-ttu-id="417d3-127">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="417d3-127">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417d3-128">CommonParameters</span></span>
<span data-ttu-id="417d3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="417d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417d3-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="417d3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417d3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="417d3-131">INPUTS</span></span>

### <span data-ttu-id="417d3-132">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="417d3-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="417d3-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="417d3-133">OUTPUTS</span></span>

### <span data-ttu-id="417d3-134">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="417d3-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="417d3-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="417d3-135">NOTES</span></span>

## <span data-ttu-id="417d3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="417d3-136">RELATED LINKS</span></span>
