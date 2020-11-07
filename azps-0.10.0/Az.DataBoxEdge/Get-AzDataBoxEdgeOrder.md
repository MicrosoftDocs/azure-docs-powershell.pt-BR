---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 40cd719a374d5ec2fdaacfe616884b395bd24434
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776794"
---
# <span data-ttu-id="0d7fc-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="0d7fc-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="0d7fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7fc-103">Obter os detalhes do pedido para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="0d7fc-103">Get the order details for a device</span></span>

## <span data-ttu-id="0d7fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d7fc-104">SYNTAX</span></span>

### <span data-ttu-id="0d7fc-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d7fc-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d7fc-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d7fc-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d7fc-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d7fc-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d7fc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d7fc-108">DESCRIPTION</span></span>
<span data-ttu-id="0d7fc-109">O cmdlet **Get-AzDataBoxEdgeOrder** Obtém os detalhes do pedido para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="0d7fc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d7fc-110">EXAMPLES</span></span>

### <span data-ttu-id="0d7fc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d7fc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="0d7fc-112">OS</span><span class="sxs-lookup"><span data-stu-id="0d7fc-112">PARAMETERS</span></span>

### <span data-ttu-id="0d7fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7fc-113">-DefaultProfile</span></span>
<span data-ttu-id="0d7fc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d7fc-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0d7fc-115">-DeviceName</span></span>
<span data-ttu-id="0d7fc-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0d7fc-116">Resource Group Name</span></span>

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

### <span data-ttu-id="0d7fc-117">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="0d7fc-117">-DeviceObject</span></span>
<span data-ttu-id="0d7fc-118">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="0d7fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d7fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d7fc-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0d7fc-120">Resource Group Name</span></span>

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

### <span data-ttu-id="0d7fc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d7fc-121">-ResourceId</span></span>
<span data-ttu-id="0d7fc-122">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="0d7fc-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="0d7fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7fc-123">CommonParameters</span></span>
<span data-ttu-id="0d7fc-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7fc-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d7fc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7fc-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d7fc-126">INPUTS</span></span>

### <span data-ttu-id="0d7fc-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0d7fc-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="0d7fc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0d7fc-128">System.String</span></span>

## <span data-ttu-id="0d7fc-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d7fc-129">OUTPUTS</span></span>

### <span data-ttu-id="0d7fc-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="0d7fc-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="0d7fc-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d7fc-131">NOTES</span></span>

## <span data-ttu-id="0d7fc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d7fc-132">RELATED LINKS</span></span>