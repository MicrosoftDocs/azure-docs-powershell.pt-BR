---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 96c9b736398cb981dd055d072091aa24af4d3f6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776785"
---
# <span data-ttu-id="5b946-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5b946-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="5b946-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b946-102">SYNOPSIS</span></span>
<span data-ttu-id="5b946-103">Obter os gatilhos configurados em um dispositivo</span><span class="sxs-lookup"><span data-stu-id="5b946-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="5b946-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b946-104">SYNTAX</span></span>

### <span data-ttu-id="5b946-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5b946-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b946-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b946-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b946-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b946-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b946-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b946-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5b946-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b946-109">DESCRIPTION</span></span>
<span data-ttu-id="5b946-110">O cmdlet **Get-AzDataBoxEdgeTriger** Obtém os gatilhos de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b946-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="5b946-111">Você pode especificar o nome como um parâmetro no cmdlet para buscar os detalhes de um gatilho específico específico</span><span class="sxs-lookup"><span data-stu-id="5b946-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="5b946-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b946-112">EXAMPLES</span></span>

### <span data-ttu-id="5b946-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b946-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="5b946-114">OS</span><span class="sxs-lookup"><span data-stu-id="5b946-114">PARAMETERS</span></span>

### <span data-ttu-id="5b946-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b946-115">-DefaultProfile</span></span>
<span data-ttu-id="5b946-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b946-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b946-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5b946-117">-DeviceName</span></span>
<span data-ttu-id="5b946-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="5b946-118">Device Name</span></span>

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

### <span data-ttu-id="5b946-119">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="5b946-119">-DeviceObject</span></span>
<span data-ttu-id="5b946-120">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="5b946-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="5b946-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b946-121">-Name</span></span>
<span data-ttu-id="5b946-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="5b946-122">Resource Name</span></span>

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

### <span data-ttu-id="5b946-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b946-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b946-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5b946-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5b946-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b946-125">-ResourceId</span></span>
<span data-ttu-id="5b946-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="5b946-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="5b946-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b946-127">CommonParameters</span></span>
<span data-ttu-id="5b946-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b946-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b946-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b946-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b946-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b946-130">INPUTS</span></span>

### <span data-ttu-id="5b946-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5b946-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="5b946-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b946-132">OUTPUTS</span></span>

### <span data-ttu-id="5b946-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5b946-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="5b946-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b946-134">NOTES</span></span>

## <span data-ttu-id="5b946-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b946-135">RELATED LINKS</span></span>