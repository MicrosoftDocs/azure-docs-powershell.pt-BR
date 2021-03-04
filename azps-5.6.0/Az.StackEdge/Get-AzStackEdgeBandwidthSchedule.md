---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: e13992fdd8a14a75c859312b62833dc66b2e539a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893084"
---
# <span data-ttu-id="059f1-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="059f1-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="059f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059f1-102">SYNOPSIS</span></span>
<span data-ttu-id="059f1-103">Obtém as informações sobre os agendamentos de largura de banda</span><span class="sxs-lookup"><span data-stu-id="059f1-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="059f1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="059f1-104">SYNTAX</span></span>

### <span data-ttu-id="059f1-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="059f1-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="059f1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="059f1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="059f1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="059f1-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="059f1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="059f1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="059f1-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="059f1-109">DESCRIPTION</span></span>
<span data-ttu-id="059f1-110">O cmdlet **Get-AzStackEdgeBandwidthSchedule** obtém as informações sobre os Cronogramas de Largura de Banda.</span><span class="sxs-lookup"><span data-stu-id="059f1-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="059f1-111">Você pode especificar o Nome de um Cronograma juntamente com o nome do Grupo de Recursos e o nome do dispositivo para obter as informações sobre um cronograma de largura de banda específico</span><span class="sxs-lookup"><span data-stu-id="059f1-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="059f1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="059f1-112">EXAMPLES</span></span>

### <span data-ttu-id="059f1-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="059f1-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="059f1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="059f1-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="059f1-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="059f1-115">PARAMETERS</span></span>

### <span data-ttu-id="059f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059f1-116">-DefaultProfile</span></span>
<span data-ttu-id="059f1-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="059f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="059f1-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="059f1-118">-DeviceName</span></span>
<span data-ttu-id="059f1-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="059f1-119">Device Name</span></span>

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

### <span data-ttu-id="059f1-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="059f1-120">-DeviceObject</span></span>
<span data-ttu-id="059f1-121">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="059f1-121">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="059f1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="059f1-122">-Name</span></span>
<span data-ttu-id="059f1-123">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="059f1-123">Resource Name</span></span>

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

### <span data-ttu-id="059f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="059f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="059f1-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="059f1-125">Resource Group Name</span></span>

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

### <span data-ttu-id="059f1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="059f1-126">-ResourceId</span></span>
<span data-ttu-id="059f1-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="059f1-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="059f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059f1-128">CommonParameters</span></span>
<span data-ttu-id="059f1-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059f1-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="059f1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059f1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="059f1-131">INPUTS</span></span>

### <span data-ttu-id="059f1-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="059f1-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="059f1-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="059f1-133">OUTPUTS</span></span>

### <span data-ttu-id="059f1-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="059f1-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="059f1-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="059f1-135">NOTES</span></span>

## <span data-ttu-id="059f1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="059f1-136">RELATED LINKS</span></span>
