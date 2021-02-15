---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111994"
---
# <span data-ttu-id="f2ccb-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f2ccb-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="f2ccb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ccb-103">Obter os detalhes do pedido de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="f2ccb-103">Get the order details for a device</span></span>

## <span data-ttu-id="f2ccb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2ccb-104">SYNTAX</span></span>

### <span data-ttu-id="f2ccb-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2ccb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2ccb-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2ccb-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2ccb-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2ccb-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2ccb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2ccb-108">DESCRIPTION</span></span>
<span data-ttu-id="f2ccb-109">O cmdlet **Get-AzDataBoxEdgeOrder** obtém os detalhes do pedido de um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="f2ccb-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="f2ccb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2ccb-110">EXAMPLES</span></span>

### <span data-ttu-id="f2ccb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2ccb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="f2ccb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2ccb-112">PARAMETERS</span></span>

### <span data-ttu-id="f2ccb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ccb-113">-DefaultProfile</span></span>
<span data-ttu-id="f2ccb-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ccb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2ccb-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f2ccb-115">-DeviceName</span></span>
<span data-ttu-id="f2ccb-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f2ccb-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f2ccb-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f2ccb-117">-DeviceObject</span></span>
<span data-ttu-id="f2ccb-118">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="f2ccb-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="f2ccb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ccb-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2ccb-120">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f2ccb-120">Resource Group Name</span></span>

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

### <span data-ttu-id="f2ccb-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2ccb-121">-ResourceId</span></span>
<span data-ttu-id="f2ccb-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2ccb-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="f2ccb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ccb-123">CommonParameters</span></span>
<span data-ttu-id="f2ccb-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ccb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ccb-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2ccb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ccb-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="f2ccb-126">INPUTS</span></span>

### <span data-ttu-id="f2ccb-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f2ccb-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="f2ccb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f2ccb-128">System.String</span></span>

## <span data-ttu-id="f2ccb-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="f2ccb-129">OUTPUTS</span></span>

### <span data-ttu-id="f2ccb-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f2ccb-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="f2ccb-131">Notas</span><span class="sxs-lookup"><span data-stu-id="f2ccb-131">NOTES</span></span>

## <span data-ttu-id="f2ccb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2ccb-132">RELATED LINKS</span></span>
