---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117765"
---
# <span data-ttu-id="c690e-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="c690e-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="c690e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c690e-102">SYNOPSIS</span></span>
<span data-ttu-id="c690e-103">Busca as funções disponíveis para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c690e-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="c690e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c690e-104">SYNTAX</span></span>

### <span data-ttu-id="c690e-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c690e-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c690e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c690e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c690e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c690e-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c690e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c690e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c690e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c690e-109">DESCRIPTION</span></span>
<span data-ttu-id="c690e-110">O cmdlet **Get-AzDataBoxEdgeRole** busca as funções de IoT disponíveis para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="c690e-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="c690e-111">Você pode mencionar o parâmetro Nome para obter os detalhes de uma função IoT específica.</span><span class="sxs-lookup"><span data-stu-id="c690e-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="c690e-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c690e-112">EXAMPLES</span></span>

### <span data-ttu-id="c690e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c690e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="c690e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c690e-114">PARAMETERS</span></span>

### <span data-ttu-id="c690e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c690e-115">-DefaultProfile</span></span>
<span data-ttu-id="c690e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c690e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c690e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c690e-117">-DeviceName</span></span>
<span data-ttu-id="c690e-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c690e-118">Device Name</span></span>

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

### <span data-ttu-id="c690e-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c690e-119">-DeviceObject</span></span>
<span data-ttu-id="c690e-120">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="c690e-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c690e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c690e-121">-Name</span></span>
<span data-ttu-id="c690e-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="c690e-122">Resource Name</span></span>

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

### <span data-ttu-id="c690e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c690e-123">-ResourceGroupName</span></span>
<span data-ttu-id="c690e-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c690e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c690e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c690e-125">-ResourceId</span></span>
<span data-ttu-id="c690e-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c690e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="c690e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c690e-127">CommonParameters</span></span>
<span data-ttu-id="c690e-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c690e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c690e-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c690e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c690e-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="c690e-130">INPUTS</span></span>

### <span data-ttu-id="c690e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c690e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c690e-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="c690e-132">OUTPUTS</span></span>

### <span data-ttu-id="c690e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="c690e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="c690e-134">Notas</span><span class="sxs-lookup"><span data-stu-id="c690e-134">NOTES</span></span>

## <span data-ttu-id="c690e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c690e-135">RELATED LINKS</span></span>
