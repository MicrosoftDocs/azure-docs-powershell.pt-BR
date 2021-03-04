---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 104313bf635f82250172fb2f34889c93a3dc92c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891390"
---
# <span data-ttu-id="d334d-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d334d-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="d334d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d334d-102">SYNOPSIS</span></span>
<span data-ttu-id="d334d-103">Obter os detalhes do pedido para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="d334d-103">Get the order details for a device</span></span>

## <span data-ttu-id="d334d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d334d-104">SYNTAX</span></span>

### <span data-ttu-id="d334d-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d334d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d334d-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d334d-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d334d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d334d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d334d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d334d-108">DESCRIPTION</span></span>
<span data-ttu-id="d334d-109">O cmdlet **Get-AzDataBoxEdgeOrder** obtém os detalhes do pedido de um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="d334d-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="d334d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d334d-110">EXAMPLES</span></span>

### <span data-ttu-id="d334d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d334d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="d334d-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d334d-112">PARAMETERS</span></span>

### <span data-ttu-id="d334d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d334d-113">-DefaultProfile</span></span>
<span data-ttu-id="d334d-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d334d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d334d-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d334d-115">-DeviceName</span></span>
<span data-ttu-id="d334d-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d334d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d334d-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d334d-117">-DeviceObject</span></span>
<span data-ttu-id="d334d-118">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="d334d-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d334d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d334d-119">-ResourceGroupName</span></span>
<span data-ttu-id="d334d-120">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d334d-120">Resource Group Name</span></span>

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

### <span data-ttu-id="d334d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d334d-121">-ResourceId</span></span>
<span data-ttu-id="d334d-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d334d-122">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d334d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d334d-123">CommonParameters</span></span>
<span data-ttu-id="d334d-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d334d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d334d-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d334d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d334d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d334d-126">INPUTS</span></span>

### <span data-ttu-id="d334d-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d334d-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="d334d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d334d-128">System.String</span></span>

## <span data-ttu-id="d334d-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d334d-129">OUTPUTS</span></span>

### <span data-ttu-id="d334d-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d334d-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="d334d-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="d334d-131">NOTES</span></span>

## <span data-ttu-id="d334d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d334d-132">RELATED LINKS</span></span>
