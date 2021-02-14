---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110968"
---
# <span data-ttu-id="db396-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="db396-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="db396-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db396-102">SYNOPSIS</span></span>
<span data-ttu-id="db396-103">Obtém a topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="db396-103">Gets the service topology.</span></span>

## <span data-ttu-id="db396-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db396-104">SYNTAX</span></span>

### <span data-ttu-id="db396-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db396-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db396-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="db396-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db396-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="db396-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db396-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="db396-108">DESCRIPTION</span></span>
<span data-ttu-id="db396-109">O cmdlet **Get-AzDeploymentManagerServiceTopology** obtém uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="db396-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="db396-110">Você pode modificar esse objeto localmente e aplicar alterações à topologia usando o cmdlet Set-AzDeploymentManagerServiceTopology texto.</span><span class="sxs-lookup"><span data-stu-id="db396-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="db396-111">Especifique a topologia do serviço pelo nome e pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db396-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="db396-112">Como alternativa, você pode fornecer o objeto ServiceTopology ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="db396-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="db396-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db396-113">EXAMPLES</span></span>

### <span data-ttu-id="db396-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db396-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="db396-115">Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="db396-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="db396-116">Exemplo 2: Obter uma topologia de serviço usando o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="db396-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="db396-117">Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="db396-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="db396-118">Exemplo 3: Obter uma topologia de serviço usando o objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="db396-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="db396-119">Esse comando obtém uma topologia de serviço cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="db396-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="db396-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db396-120">PARAMETERS</span></span>

### <span data-ttu-id="db396-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db396-121">-DefaultProfile</span></span>
<span data-ttu-id="db396-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db396-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db396-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db396-123">-InputObject</span></span>
<span data-ttu-id="db396-124">Objeto de recurso de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="db396-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="db396-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="db396-125">-Name</span></span>
<span data-ttu-id="db396-126">O nome da topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="db396-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="db396-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db396-127">-ResourceGroupName</span></span>
<span data-ttu-id="db396-128">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db396-128">The resource group.</span></span>

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

### <span data-ttu-id="db396-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db396-129">-ResourceId</span></span>
<span data-ttu-id="db396-130">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="db396-130">The resource identifier.</span></span>

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

### <span data-ttu-id="db396-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db396-131">CommonParameters</span></span>
<span data-ttu-id="db396-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db396-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db396-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db396-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db396-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="db396-134">INPUTS</span></span>

### <span data-ttu-id="db396-135">System.String</span><span class="sxs-lookup"><span data-stu-id="db396-135">System.String</span></span>

### <span data-ttu-id="db396-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="db396-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="db396-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="db396-137">OUTPUTS</span></span>

### <span data-ttu-id="db396-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="db396-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="db396-139">Notas</span><span class="sxs-lookup"><span data-stu-id="db396-139">NOTES</span></span>

## <span data-ttu-id="db396-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db396-140">RELATED LINKS</span></span>
