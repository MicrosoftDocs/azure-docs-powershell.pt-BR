---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: c4d33dad9377c6ee53452c90b5d582413e2eee73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886713"
---
# <span data-ttu-id="d37e8-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d37e8-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="d37e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d37e8-103">Busca as funções disponíveis para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d37e8-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="d37e8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d37e8-104">SYNTAX</span></span>

### <span data-ttu-id="d37e8-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d37e8-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d37e8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d37e8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d37e8-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d37e8-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d37e8-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d37e8-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="d37e8-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d37e8-109">DESCRIPTION</span></span>
<span data-ttu-id="d37e8-110">O cmdlet **Get-AzStackEdgeRole** busca as funções de IoT disponíveis para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="d37e8-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="d37e8-111">Você pode mencionar o parâmetro Name para obter os detalhes de uma função IoT específica.</span><span class="sxs-lookup"><span data-stu-id="d37e8-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="d37e8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d37e8-112">EXAMPLES</span></span>

### <span data-ttu-id="d37e8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d37e8-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="d37e8-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d37e8-114">PARAMETERS</span></span>

### <span data-ttu-id="d37e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37e8-115">-DefaultProfile</span></span>
<span data-ttu-id="d37e8-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d37e8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37e8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d37e8-117">-DeviceName</span></span>
<span data-ttu-id="d37e8-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d37e8-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e8-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d37e8-119">-DeviceObject</span></span>
<span data-ttu-id="d37e8-120">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="d37e8-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d37e8-121">-Name</span></span>
<span data-ttu-id="d37e8-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="d37e8-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37e8-123">-ResourceGroupName</span></span>
<span data-ttu-id="d37e8-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d37e8-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d37e8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d37e8-125">-ResourceId</span></span>
<span data-ttu-id="d37e8-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d37e8-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="d37e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37e8-127">CommonParameters</span></span>
<span data-ttu-id="d37e8-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37e8-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d37e8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37e8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d37e8-130">INPUTS</span></span>

### <span data-ttu-id="d37e8-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d37e8-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="d37e8-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d37e8-132">OUTPUTS</span></span>

### <span data-ttu-id="d37e8-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d37e8-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="d37e8-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="d37e8-134">NOTES</span></span>

## <span data-ttu-id="d37e8-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d37e8-135">RELATED LINKS</span></span>
