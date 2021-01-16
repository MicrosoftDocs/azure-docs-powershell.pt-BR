---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433973"
---
# <span data-ttu-id="41706-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="41706-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="41706-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41706-102">SYNOPSIS</span></span>
<span data-ttu-id="41706-103">Busca as funções disponíveis para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41706-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="41706-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41706-104">SYNTAX</span></span>

### <span data-ttu-id="41706-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="41706-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41706-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41706-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41706-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="41706-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41706-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41706-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="41706-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41706-109">DESCRIPTION</span></span>
<span data-ttu-id="41706-110">O cmdlet **Get-AzDataBoxEdgeRole** busca as funções IOT disponíveis para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="41706-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="41706-111">Você pode mencionar o parâmetro Name para obter os detalhes de uma função IoT específica.</span><span class="sxs-lookup"><span data-stu-id="41706-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="41706-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41706-112">EXAMPLES</span></span>

### <span data-ttu-id="41706-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41706-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="41706-114">OS</span><span class="sxs-lookup"><span data-stu-id="41706-114">PARAMETERS</span></span>

### <span data-ttu-id="41706-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41706-115">-DefaultProfile</span></span>
<span data-ttu-id="41706-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41706-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41706-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="41706-117">-DeviceName</span></span>
<span data-ttu-id="41706-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="41706-118">Device Name</span></span>

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

### <span data-ttu-id="41706-119">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="41706-119">-DeviceObject</span></span>
<span data-ttu-id="41706-120">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="41706-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="41706-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="41706-121">-Name</span></span>
<span data-ttu-id="41706-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="41706-122">Resource Name</span></span>

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

### <span data-ttu-id="41706-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41706-123">-ResourceGroupName</span></span>
<span data-ttu-id="41706-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="41706-124">Resource Group Name</span></span>

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

### <span data-ttu-id="41706-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41706-125">-ResourceId</span></span>
<span data-ttu-id="41706-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="41706-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="41706-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41706-127">CommonParameters</span></span>
<span data-ttu-id="41706-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41706-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41706-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41706-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41706-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41706-130">INPUTS</span></span>

### <span data-ttu-id="41706-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="41706-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="41706-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41706-132">OUTPUTS</span></span>

### <span data-ttu-id="41706-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="41706-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="41706-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41706-134">NOTES</span></span>

## <span data-ttu-id="41706-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41706-135">RELATED LINKS</span></span>
