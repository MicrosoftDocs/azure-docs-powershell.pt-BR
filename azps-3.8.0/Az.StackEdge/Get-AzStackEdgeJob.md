---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941069"
---
# <span data-ttu-id="56cf7-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="56cf7-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="56cf7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="56cf7-103">Obtém os trabalhos agendados em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56cf7-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="56cf7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56cf7-104">SYNTAX</span></span>

### <span data-ttu-id="56cf7-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="56cf7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56cf7-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="56cf7-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56cf7-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56cf7-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="56cf7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56cf7-108">DESCRIPTION</span></span>
<span data-ttu-id="56cf7-109">O cmdlet **Get-AzStackEdgeJob** Obtém os trabalhos ativos em um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="56cf7-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="56cf7-110">Você pode mencionar o parâmetro Name para obter detalhes de um trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="56cf7-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="56cf7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56cf7-111">EXAMPLES</span></span>

### <span data-ttu-id="56cf7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56cf7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="56cf7-113">OS</span><span class="sxs-lookup"><span data-stu-id="56cf7-113">PARAMETERS</span></span>

### <span data-ttu-id="56cf7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56cf7-114">-DefaultProfile</span></span>
<span data-ttu-id="56cf7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56cf7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56cf7-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="56cf7-116">-DeviceName</span></span>
<span data-ttu-id="56cf7-117">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="56cf7-117">Name of the device</span></span>

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

### <span data-ttu-id="56cf7-118">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="56cf7-118">-DeviceObject</span></span>
<span data-ttu-id="56cf7-119">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="56cf7-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="56cf7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="56cf7-120">-Name</span></span>
<span data-ttu-id="56cf7-121">Nome do trabalho, geralmente um GUID</span><span class="sxs-lookup"><span data-stu-id="56cf7-121">Name of the Job, Generally a GUID</span></span>

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

### <span data-ttu-id="56cf7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56cf7-122">-ResourceGroupName</span></span>
<span data-ttu-id="56cf7-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="56cf7-123">Resource Group Name</span></span>

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

### <span data-ttu-id="56cf7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56cf7-124">-ResourceId</span></span>
<span data-ttu-id="56cf7-125">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="56cf7-125">Azure ResourceId</span></span>

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

### <span data-ttu-id="56cf7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56cf7-126">CommonParameters</span></span>
<span data-ttu-id="56cf7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56cf7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56cf7-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56cf7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56cf7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56cf7-129">INPUTS</span></span>

### <span data-ttu-id="56cf7-130">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="56cf7-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="56cf7-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56cf7-131">OUTPUTS</span></span>

### <span data-ttu-id="56cf7-132">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="56cf7-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="56cf7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56cf7-133">NOTES</span></span>

## <span data-ttu-id="56cf7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56cf7-134">RELATED LINKS</span></span>
