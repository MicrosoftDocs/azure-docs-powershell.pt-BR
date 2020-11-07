---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e3453e3359bb800180ebdeb3fa5158b890fd237a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942165"
---
# <span data-ttu-id="a2b20-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a2b20-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a2b20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2b20-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b20-103">Obtém as informações sobre as agendas de largura de banda</span><span class="sxs-lookup"><span data-stu-id="a2b20-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="a2b20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2b20-104">SYNTAX</span></span>

### <span data-ttu-id="a2b20-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a2b20-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2b20-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2b20-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2b20-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2b20-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2b20-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2b20-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a2b20-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2b20-109">DESCRIPTION</span></span>
<span data-ttu-id="a2b20-110">O cmdlet **Get-AzDataBoxEdgeBandwidthSchedule** Obtém as informações sobre as agendas de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="a2b20-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="a2b20-111">Você pode especificar o nome de um cronograma juntamente com o nome do grupo de recursos e o nome do dispositivo para obter as informações sobre um agendamento de largura de banda específico</span><span class="sxs-lookup"><span data-stu-id="a2b20-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="a2b20-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2b20-112">EXAMPLES</span></span>

### <span data-ttu-id="a2b20-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2b20-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="a2b20-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a2b20-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="a2b20-115">OS</span><span class="sxs-lookup"><span data-stu-id="a2b20-115">PARAMETERS</span></span>

### <span data-ttu-id="a2b20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b20-116">-DefaultProfile</span></span>
<span data-ttu-id="a2b20-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2b20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2b20-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a2b20-118">-DeviceName</span></span>
<span data-ttu-id="a2b20-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="a2b20-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b20-120">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="a2b20-120">-DeviceObject</span></span>
<span data-ttu-id="a2b20-121">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="a2b20-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b20-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2b20-122">-Name</span></span>
<span data-ttu-id="a2b20-123">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="a2b20-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b20-124">-ResourceGroupName</span></span>
<span data-ttu-id="a2b20-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a2b20-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b20-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2b20-126">-ResourceId</span></span>
<span data-ttu-id="a2b20-127">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="a2b20-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="a2b20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b20-128">CommonParameters</span></span>
<span data-ttu-id="a2b20-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b20-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2b20-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b20-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2b20-131">INPUTS</span></span>

### <span data-ttu-id="a2b20-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a2b20-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a2b20-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2b20-133">OUTPUTS</span></span>

### <span data-ttu-id="a2b20-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a2b20-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a2b20-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2b20-135">NOTES</span></span>

## <span data-ttu-id="a2b20-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2b20-136">RELATED LINKS</span></span>
