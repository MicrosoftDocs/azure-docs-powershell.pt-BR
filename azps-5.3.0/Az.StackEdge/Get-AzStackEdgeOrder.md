---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433800"
---
# <span data-ttu-id="3608c-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="3608c-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="3608c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3608c-102">SYNOPSIS</span></span>
<span data-ttu-id="3608c-103">Obter os detalhes do pedido para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="3608c-103">Get the order details for a device</span></span>

## <span data-ttu-id="3608c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3608c-104">SYNTAX</span></span>

### <span data-ttu-id="3608c-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3608c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3608c-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3608c-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3608c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3608c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3608c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3608c-108">DESCRIPTION</span></span>
<span data-ttu-id="3608c-109">O cmdlet **Get-AzStackEdgeOrder** Obtém os detalhes do pedido para um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="3608c-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="3608c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3608c-110">EXAMPLES</span></span>

### <span data-ttu-id="3608c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3608c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="3608c-112">OS</span><span class="sxs-lookup"><span data-stu-id="3608c-112">PARAMETERS</span></span>

### <span data-ttu-id="3608c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3608c-113">-DefaultProfile</span></span>
<span data-ttu-id="3608c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3608c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3608c-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3608c-115">-DeviceName</span></span>
<span data-ttu-id="3608c-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3608c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="3608c-117">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="3608c-117">-DeviceObject</span></span>
<span data-ttu-id="3608c-118">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="3608c-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3608c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3608c-119">-ResourceGroupName</span></span>
<span data-ttu-id="3608c-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3608c-120">Resource Group Name</span></span>

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

### <span data-ttu-id="3608c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3608c-121">-ResourceId</span></span>
<span data-ttu-id="3608c-122">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="3608c-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="3608c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3608c-123">CommonParameters</span></span>
<span data-ttu-id="3608c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3608c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3608c-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3608c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3608c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3608c-126">INPUTS</span></span>

### <span data-ttu-id="3608c-127">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3608c-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="3608c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3608c-128">System.String</span></span>

## <span data-ttu-id="3608c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3608c-129">OUTPUTS</span></span>

### <span data-ttu-id="3608c-130">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="3608c-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="3608c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3608c-131">NOTES</span></span>

## <span data-ttu-id="3608c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3608c-132">RELATED LINKS</span></span>
