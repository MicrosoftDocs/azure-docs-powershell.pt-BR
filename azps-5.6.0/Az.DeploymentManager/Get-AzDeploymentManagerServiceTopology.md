---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c02a88cdb550e1ec9cb343b286d3211045873820
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888977"
---
# <span data-ttu-id="c49b0-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c49b0-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="c49b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c49b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c49b0-103">Obtém a topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="c49b0-103">Gets the service topology.</span></span>

## <span data-ttu-id="c49b0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c49b0-104">SYNTAX</span></span>

### <span data-ttu-id="c49b0-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c49b0-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c49b0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c49b0-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c49b0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c49b0-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c49b0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c49b0-108">DESCRIPTION</span></span>
<span data-ttu-id="c49b0-109">O cmdlet **Get-AzDeploymentManagerServiceTopology** obtém uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="c49b0-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="c49b0-110">Você pode modificar esse objeto localmente e aplicar alterações à topologia usando o cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c49b0-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="c49b0-111">Especifique a topologia de serviço pelo nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c49b0-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="c49b0-112">Como alternativa, você pode fornecer o objeto ServiceTopology ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c49b0-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="c49b0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c49b0-113">EXAMPLES</span></span>

### <span data-ttu-id="c49b0-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c49b0-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="c49b0-115">Este comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c49b0-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c49b0-116">Exemplo 2: Obter uma topologia de serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="c49b0-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="c49b0-117">Este comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c49b0-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c49b0-118">Exemplo 3: Obter uma topologia de serviço usando o objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="c49b0-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="c49b0-119">Este comando obtém uma topologia de serviço cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c49b0-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="c49b0-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c49b0-120">PARAMETERS</span></span>

### <span data-ttu-id="c49b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49b0-121">-DefaultProfile</span></span>
<span data-ttu-id="c49b0-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c49b0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c49b0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c49b0-123">-InputObject</span></span>
<span data-ttu-id="c49b0-124">Objeto de recurso de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="c49b0-124">Service topology resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c49b0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c49b0-125">-Name</span></span>
<span data-ttu-id="c49b0-126">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="c49b0-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c49b0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49b0-127">-ResourceGroupName</span></span>
<span data-ttu-id="c49b0-128">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c49b0-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c49b0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c49b0-129">-ResourceId</span></span>
<span data-ttu-id="c49b0-130">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="c49b0-130">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c49b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49b0-131">CommonParameters</span></span>
<span data-ttu-id="c49b0-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c49b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49b0-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c49b0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49b0-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c49b0-134">INPUTS</span></span>

### <span data-ttu-id="c49b0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c49b0-135">System.String</span></span>

### <span data-ttu-id="c49b0-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c49b0-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c49b0-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c49b0-137">OUTPUTS</span></span>

### <span data-ttu-id="c49b0-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c49b0-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c49b0-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="c49b0-139">NOTES</span></span>

## <span data-ttu-id="c49b0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c49b0-140">RELATED LINKS</span></span>
