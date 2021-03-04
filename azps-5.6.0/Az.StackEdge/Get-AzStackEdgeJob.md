---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 14e19068d3634acfd558f976b13661af28495321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892599"
---
# <span data-ttu-id="7e7fa-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="7e7fa-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="7e7fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7fa-103">Obtém os trabalhos agendados em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="7e7fa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7e7fa-104">SYNTAX</span></span>

### <span data-ttu-id="7e7fa-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7e7fa-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e7fa-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="7e7fa-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e7fa-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7fa-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="7e7fa-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7e7fa-108">DESCRIPTION</span></span>
<span data-ttu-id="7e7fa-109">O cmdlet **Get-AzStackEdgeJob** obtém os trabalhos ativos em um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="7e7fa-110">Você pode mencionar o parâmetro Name para obter detalhes de um trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="7e7fa-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e7fa-111">EXAMPLES</span></span>

### <span data-ttu-id="7e7fa-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e7fa-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="7e7fa-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7e7fa-113">PARAMETERS</span></span>

### <span data-ttu-id="7e7fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7fa-114">-DefaultProfile</span></span>
<span data-ttu-id="7e7fa-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e7fa-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7e7fa-116">-DeviceName</span></span>
<span data-ttu-id="7e7fa-117">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="7e7fa-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7fa-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7e7fa-118">-DeviceObject</span></span>
<span data-ttu-id="7e7fa-119">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="7e7fa-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7fa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7e7fa-120">-Name</span></span>
<span data-ttu-id="7e7fa-121">Nome do trabalho, geralmente um GUID</span><span class="sxs-lookup"><span data-stu-id="7e7fa-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e7fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="7e7fa-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7e7fa-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7fa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e7fa-124">-ResourceId</span></span>
<span data-ttu-id="7e7fa-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e7fa-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7fa-126">CommonParameters</span></span>
<span data-ttu-id="7e7fa-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e7fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7fa-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e7fa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7fa-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e7fa-129">INPUTS</span></span>

### <span data-ttu-id="7e7fa-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7e7fa-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="7e7fa-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7e7fa-131">OUTPUTS</span></span>

### <span data-ttu-id="7e7fa-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="7e7fa-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="7e7fa-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="7e7fa-133">NOTES</span></span>

## <span data-ttu-id="7e7fa-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e7fa-134">RELATED LINKS</span></span>
