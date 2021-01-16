---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256877"
---
# <span data-ttu-id="958ac-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="958ac-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="958ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="958ac-102">SYNOPSIS</span></span>
<span data-ttu-id="958ac-103">Obtém a topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="958ac-103">Gets the service topology.</span></span>

## <span data-ttu-id="958ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="958ac-104">SYNTAX</span></span>

### <span data-ttu-id="958ac-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="958ac-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958ac-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="958ac-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="958ac-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="958ac-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="958ac-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="958ac-108">DESCRIPTION</span></span>
<span data-ttu-id="958ac-109">O cmdlet **Get-AzDeploymentManagerServiceTopology** Obtém uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="958ac-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="958ac-110">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações à topologia usando o cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="958ac-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="958ac-111">Especifique a topologia do serviço de acordo com o nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="958ac-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="958ac-112">Como alternativa, você pode fornecer o objeto imtopology ou o resourceId.</span><span class="sxs-lookup"><span data-stu-id="958ac-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="958ac-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="958ac-113">EXAMPLES</span></span>

### <span data-ttu-id="958ac-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="958ac-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="958ac-115">Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="958ac-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="958ac-116">Exemplo 2: obter uma topologia de serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="958ac-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="958ac-117">Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="958ac-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="958ac-118">Exemplo 3: obter uma topologia de serviço usando o objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="958ac-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="958ac-119">Esse comando obtém uma topologia de serviço cujo nome e o meu nome de fonte correspondem às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="958ac-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="958ac-120">OS</span><span class="sxs-lookup"><span data-stu-id="958ac-120">PARAMETERS</span></span>

### <span data-ttu-id="958ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958ac-121">-DefaultProfile</span></span>
<span data-ttu-id="958ac-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="958ac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="958ac-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="958ac-123">-InputObject</span></span>
<span data-ttu-id="958ac-124">Objeto de recurso de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="958ac-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="958ac-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="958ac-125">-Name</span></span>
<span data-ttu-id="958ac-126">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="958ac-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="958ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="958ac-128">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="958ac-128">The resource group.</span></span>

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

### <span data-ttu-id="958ac-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="958ac-129">-ResourceId</span></span>
<span data-ttu-id="958ac-130">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="958ac-130">The resource identifier.</span></span>

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

### <span data-ttu-id="958ac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958ac-131">CommonParameters</span></span>
<span data-ttu-id="958ac-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958ac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958ac-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="958ac-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958ac-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="958ac-134">INPUTS</span></span>

### <span data-ttu-id="958ac-135">System. String</span><span class="sxs-lookup"><span data-stu-id="958ac-135">System.String</span></span>

### <span data-ttu-id="958ac-136">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="958ac-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="958ac-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="958ac-137">OUTPUTS</span></span>

### <span data-ttu-id="958ac-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="958ac-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="958ac-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="958ac-139">NOTES</span></span>

## <span data-ttu-id="958ac-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="958ac-140">RELATED LINKS</span></span>
