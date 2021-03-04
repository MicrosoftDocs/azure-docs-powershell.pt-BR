---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9dd4925224f2ed91770caff422b8ab6f5d924754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891470"
---
# <span data-ttu-id="8cbfc-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8cbfc-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="8cbfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbfc-103">Busca as funções disponíveis para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8cbfc-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="8cbfc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8cbfc-104">SYNTAX</span></span>

### <span data-ttu-id="8cbfc-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8cbfc-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbfc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cbfc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbfc-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cbfc-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbfc-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cbfc-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8cbfc-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8cbfc-109">DESCRIPTION</span></span>
<span data-ttu-id="8cbfc-110">O cmdlet **Get-AzDataBoxEdgeRole** busca as funções de IoT disponíveis para um dispositivo de Borda de Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="8cbfc-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="8cbfc-111">Você pode mencionar o parâmetro Name para obter os detalhes de uma função IoT específica.</span><span class="sxs-lookup"><span data-stu-id="8cbfc-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="8cbfc-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cbfc-112">EXAMPLES</span></span>

### <span data-ttu-id="8cbfc-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8cbfc-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="8cbfc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8cbfc-114">PARAMETERS</span></span>

### <span data-ttu-id="8cbfc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbfc-115">-DefaultProfile</span></span>
<span data-ttu-id="8cbfc-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cbfc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cbfc-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8cbfc-117">-DeviceName</span></span>
<span data-ttu-id="8cbfc-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8cbfc-118">Device Name</span></span>

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

### <span data-ttu-id="8cbfc-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8cbfc-119">-DeviceObject</span></span>
<span data-ttu-id="8cbfc-120">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="8cbfc-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8cbfc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8cbfc-121">-Name</span></span>
<span data-ttu-id="8cbfc-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="8cbfc-122">Resource Name</span></span>

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

### <span data-ttu-id="8cbfc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cbfc-123">-ResourceGroupName</span></span>
<span data-ttu-id="8cbfc-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8cbfc-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8cbfc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cbfc-125">-ResourceId</span></span>
<span data-ttu-id="8cbfc-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cbfc-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="8cbfc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbfc-127">CommonParameters</span></span>
<span data-ttu-id="8cbfc-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cbfc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbfc-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cbfc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbfc-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8cbfc-130">INPUTS</span></span>

### <span data-ttu-id="8cbfc-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8cbfc-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8cbfc-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8cbfc-132">OUTPUTS</span></span>

### <span data-ttu-id="8cbfc-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8cbfc-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="8cbfc-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="8cbfc-134">NOTES</span></span>

## <span data-ttu-id="8cbfc-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cbfc-135">RELATED LINKS</span></span>
