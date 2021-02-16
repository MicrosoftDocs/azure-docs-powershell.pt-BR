---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113696"
---
# <span data-ttu-id="7c070-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="7c070-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="7c070-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c070-102">SYNOPSIS</span></span>
<span data-ttu-id="7c070-103">Obter os detalhes do pedido de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="7c070-103">Get the order details for a device</span></span>

## <span data-ttu-id="7c070-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c070-104">SYNTAX</span></span>

### <span data-ttu-id="7c070-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7c070-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c070-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c070-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c070-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c070-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c070-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c070-108">DESCRIPTION</span></span>
<span data-ttu-id="7c070-109">O **cmdlet Get-AzSt stackEdgeOrder** obtém os detalhes do pedido de um dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="7c070-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="7c070-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c070-110">EXAMPLES</span></span>

### <span data-ttu-id="7c070-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c070-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="7c070-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c070-112">PARAMETERS</span></span>

### <span data-ttu-id="7c070-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c070-113">-DefaultProfile</span></span>
<span data-ttu-id="7c070-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c070-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c070-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7c070-115">-DeviceName</span></span>
<span data-ttu-id="7c070-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7c070-116">Resource Group Name</span></span>

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

### <span data-ttu-id="7c070-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7c070-117">-DeviceObject</span></span>
<span data-ttu-id="7c070-118">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="7c070-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="7c070-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c070-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c070-120">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7c070-120">Resource Group Name</span></span>

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

### <span data-ttu-id="7c070-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c070-121">-ResourceId</span></span>
<span data-ttu-id="7c070-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c070-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="7c070-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c070-123">CommonParameters</span></span>
<span data-ttu-id="7c070-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c070-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c070-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c070-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c070-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="7c070-126">INPUTS</span></span>

### <span data-ttu-id="7c070-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7c070-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="7c070-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7c070-128">System.String</span></span>

## <span data-ttu-id="7c070-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="7c070-129">OUTPUTS</span></span>

### <span data-ttu-id="7c070-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="7c070-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="7c070-131">Notas</span><span class="sxs-lookup"><span data-stu-id="7c070-131">NOTES</span></span>

## <span data-ttu-id="7c070-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c070-132">RELATED LINKS</span></span>
