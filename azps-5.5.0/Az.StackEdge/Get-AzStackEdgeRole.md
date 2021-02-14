---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117062"
---
# <span data-ttu-id="64f2a-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="64f2a-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="64f2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="64f2a-103">Busca as funções disponíveis para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64f2a-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="64f2a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64f2a-104">SYNTAX</span></span>

### <span data-ttu-id="64f2a-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="64f2a-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64f2a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64f2a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64f2a-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64f2a-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64f2a-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64f2a-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="64f2a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="64f2a-109">DESCRIPTION</span></span>
<span data-ttu-id="64f2a-110">O cmdlet **Get-AzSt stackEdgeRole** busca as funções de IoT disponíveis para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="64f2a-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="64f2a-111">Você pode mencionar o parâmetro Nome para obter os detalhes de uma função IoT específica.</span><span class="sxs-lookup"><span data-stu-id="64f2a-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="64f2a-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64f2a-112">EXAMPLES</span></span>

### <span data-ttu-id="64f2a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64f2a-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="64f2a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64f2a-114">PARAMETERS</span></span>

### <span data-ttu-id="64f2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f2a-115">-DefaultProfile</span></span>
<span data-ttu-id="64f2a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64f2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64f2a-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="64f2a-117">-DeviceName</span></span>
<span data-ttu-id="64f2a-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="64f2a-118">Device Name</span></span>

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

### <span data-ttu-id="64f2a-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="64f2a-119">-DeviceObject</span></span>
<span data-ttu-id="64f2a-120">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="64f2a-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="64f2a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="64f2a-121">-Name</span></span>
<span data-ttu-id="64f2a-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="64f2a-122">Resource Name</span></span>

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

### <span data-ttu-id="64f2a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f2a-123">-ResourceGroupName</span></span>
<span data-ttu-id="64f2a-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="64f2a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="64f2a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64f2a-125">-ResourceId</span></span>
<span data-ttu-id="64f2a-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="64f2a-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="64f2a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f2a-127">CommonParameters</span></span>
<span data-ttu-id="64f2a-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f2a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f2a-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64f2a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f2a-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="64f2a-130">INPUTS</span></span>

### <span data-ttu-id="64f2a-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="64f2a-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="64f2a-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="64f2a-132">OUTPUTS</span></span>

### <span data-ttu-id="64f2a-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="64f2a-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="64f2a-134">Notas</span><span class="sxs-lookup"><span data-stu-id="64f2a-134">NOTES</span></span>

## <span data-ttu-id="64f2a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64f2a-135">RELATED LINKS</span></span>
