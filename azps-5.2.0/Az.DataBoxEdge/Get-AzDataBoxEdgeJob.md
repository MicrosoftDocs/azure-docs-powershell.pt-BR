---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257769"
---
# <span data-ttu-id="babf3-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="babf3-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="babf3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="babf3-102">SYNOPSIS</span></span>
<span data-ttu-id="babf3-103">Obtém os trabalhos agendados em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="babf3-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="babf3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="babf3-104">SYNTAX</span></span>

### <span data-ttu-id="babf3-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="babf3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="babf3-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="babf3-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="babf3-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="babf3-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="babf3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="babf3-108">DESCRIPTION</span></span>
<span data-ttu-id="babf3-109">O cmdlet **Get-AzDataBoxEdgeJob** Obtém os trabalhos ativos em um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="babf3-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="babf3-110">Você pode mencionar o parâmetro Name para obter detalhes de um trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="babf3-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="babf3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="babf3-111">EXAMPLES</span></span>

### <span data-ttu-id="babf3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="babf3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="babf3-113">OS</span><span class="sxs-lookup"><span data-stu-id="babf3-113">PARAMETERS</span></span>

### <span data-ttu-id="babf3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="babf3-114">-DefaultProfile</span></span>
<span data-ttu-id="babf3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="babf3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="babf3-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="babf3-116">-DeviceName</span></span>
<span data-ttu-id="babf3-117">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="babf3-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babf3-118">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="babf3-118">-DeviceObject</span></span>
<span data-ttu-id="babf3-119">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="babf3-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="babf3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="babf3-120">-Name</span></span>
<span data-ttu-id="babf3-121">Nome do trabalho, geralmente um GUID</span><span class="sxs-lookup"><span data-stu-id="babf3-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babf3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="babf3-122">-ResourceGroupName</span></span>
<span data-ttu-id="babf3-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="babf3-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babf3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="babf3-124">-ResourceId</span></span>
<span data-ttu-id="babf3-125">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="babf3-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babf3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="babf3-126">CommonParameters</span></span>
<span data-ttu-id="babf3-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="babf3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="babf3-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="babf3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="babf3-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="babf3-129">INPUTS</span></span>

### <span data-ttu-id="babf3-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="babf3-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="babf3-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="babf3-131">OUTPUTS</span></span>

### <span data-ttu-id="babf3-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="babf3-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="babf3-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="babf3-133">NOTES</span></span>

## <span data-ttu-id="babf3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="babf3-134">RELATED LINKS</span></span>
