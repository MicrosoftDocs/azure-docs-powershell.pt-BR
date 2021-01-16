---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272928"
---
# <span data-ttu-id="aeeae-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="aeeae-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="aeeae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aeeae-102">SYNOPSIS</span></span>
<span data-ttu-id="aeeae-103">Obtém a topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="aeeae-103">Gets the service topology.</span></span>

## <span data-ttu-id="aeeae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aeeae-104">SYNTAX</span></span>

### <span data-ttu-id="aeeae-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="aeeae-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeeae-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="aeeae-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aeeae-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="aeeae-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeeae-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aeeae-108">DESCRIPTION</span></span>
<span data-ttu-id="aeeae-109">O cmdlet **Get-AzDeploymentManagerServiceTopology** Obtém uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="aeeae-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="aeeae-110">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações à topologia usando o cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="aeeae-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="aeeae-111">Especifique a topologia do serviço de acordo com o nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aeeae-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="aeeae-112">Como alternativa, você pode fornecer o objeto imtopology ou o resourceId.</span><span class="sxs-lookup"><span data-stu-id="aeeae-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="aeeae-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aeeae-113">EXAMPLES</span></span>

### <span data-ttu-id="aeeae-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aeeae-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="aeeae-115">Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aeeae-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="aeeae-116">Exemplo 2: obter uma topologia de serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="aeeae-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="aeeae-117">Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aeeae-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="aeeae-118">Exemplo 3: obter uma topologia de serviço usando o objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="aeeae-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="aeeae-119">Esse comando obtém uma topologia de serviço cujo nome e o meu nome de fonte correspondem às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="aeeae-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="aeeae-120">OS</span><span class="sxs-lookup"><span data-stu-id="aeeae-120">PARAMETERS</span></span>

### <span data-ttu-id="aeeae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeeae-121">-DefaultProfile</span></span>
<span data-ttu-id="aeeae-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aeeae-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aeeae-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aeeae-123">-InputObject</span></span>
<span data-ttu-id="aeeae-124">Objeto de recurso de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="aeeae-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="aeeae-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="aeeae-125">-Name</span></span>
<span data-ttu-id="aeeae-126">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="aeeae-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="aeeae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeeae-127">-ResourceGroupName</span></span>
<span data-ttu-id="aeeae-128">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aeeae-128">The resource group.</span></span>

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

### <span data-ttu-id="aeeae-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aeeae-129">-ResourceId</span></span>
<span data-ttu-id="aeeae-130">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="aeeae-130">The resource identifier.</span></span>

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

### <span data-ttu-id="aeeae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeeae-131">CommonParameters</span></span>
<span data-ttu-id="aeeae-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeeae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeeae-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aeeae-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeeae-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aeeae-134">INPUTS</span></span>

### <span data-ttu-id="aeeae-135">System. String</span><span class="sxs-lookup"><span data-stu-id="aeeae-135">System.String</span></span>

### <span data-ttu-id="aeeae-136">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="aeeae-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="aeeae-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aeeae-137">OUTPUTS</span></span>

### <span data-ttu-id="aeeae-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="aeeae-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="aeeae-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aeeae-139">NOTES</span></span>

## <span data-ttu-id="aeeae-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aeeae-140">RELATED LINKS</span></span>
