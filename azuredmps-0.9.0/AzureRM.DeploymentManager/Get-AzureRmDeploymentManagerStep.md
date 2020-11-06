---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425733"
---
# <span data-ttu-id="7f0dd-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="7f0dd-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="7f0dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f0dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0dd-103">Obtém a etapa de implantação.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-103">Gets the deployment step.</span></span>

## <span data-ttu-id="7f0dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f0dd-104">SYNTAX</span></span>

### <span data-ttu-id="7f0dd-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f0dd-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f0dd-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="7f0dd-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f0dd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7f0dd-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f0dd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f0dd-108">DESCRIPTION</span></span>
<span data-ttu-id="7f0dd-109">O cmdlet **Get-AzureRmDeploymentManagerStep** Obtém uma etapa e retorna um objeto que representa essa etapa.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="7f0dd-110">Especifique a etapa pelo nome e pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="7f0dd-111">Como alternativa, você pode fornecer o objeto Step ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="7f0dd-112">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações à fonte de artefatos usando o cmdlet Set-AzureRmDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="7f0dd-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f0dd-113">EXAMPLES</span></span>

### <span data-ttu-id="7f0dd-114">Exemplo 1: obter uma etapa</span><span class="sxs-lookup"><span data-stu-id="7f0dd-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="7f0dd-115">Esse comando obtém uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="7f0dd-116">Exemplo 2: obter uma etapa usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="7f0dd-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="7f0dd-117">Esse comando obtém uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="7f0dd-118">Exemplo 3: obter uma etapa usando um objeto retornado por New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="7f0dd-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="7f0dd-119">Esse comando obtém uma etapa cujo nome e o meu nome do elemento de Resource correspondem às propriedades Name e ResourceGroupName do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="7f0dd-120">OS</span><span class="sxs-lookup"><span data-stu-id="7f0dd-120">PARAMETERS</span></span>

### <span data-ttu-id="7f0dd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f0dd-121">-DefaultProfile</span></span>
<span data-ttu-id="7f0dd-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0dd-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f0dd-123">-Name</span></span>
<span data-ttu-id="7f0dd-124">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-124">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f0dd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f0dd-125">-ResourceGroupName</span></span>
<span data-ttu-id="7f0dd-126">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-126">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f0dd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f0dd-127">-ResourceId</span></span>
<span data-ttu-id="7f0dd-128">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-128">The resource identifier.</span></span>

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

### <span data-ttu-id="7f0dd-129">-Etapa</span><span class="sxs-lookup"><span data-stu-id="7f0dd-129">-Step</span></span>
<span data-ttu-id="7f0dd-130">O objeto de recurso etapa.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-130">The step resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f0dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0dd-131">CommonParameters</span></span>
<span data-ttu-id="7f0dd-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f0dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7f0dd-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0dd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0dd-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f0dd-134">INPUTS</span></span>

### <span data-ttu-id="7f0dd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7f0dd-135">System.String</span></span>

### <span data-ttu-id="7f0dd-136">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="7f0dd-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="7f0dd-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f0dd-137">OUTPUTS</span></span>

### <span data-ttu-id="7f0dd-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="7f0dd-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="7f0dd-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f0dd-139">NOTES</span></span>

## <span data-ttu-id="7f0dd-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f0dd-140">RELATED LINKS</span></span>
