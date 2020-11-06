---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: eb0c7db4706aacfba4010632422869f0dca54694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596663"
---
# <span data-ttu-id="eafd4-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="eafd4-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="eafd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eafd4-102">SYNOPSIS</span></span>
<span data-ttu-id="eafd4-103">Obtém a etapa.</span><span class="sxs-lookup"><span data-stu-id="eafd4-103">Gets the step.</span></span>

## <span data-ttu-id="eafd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eafd4-104">SYNTAX</span></span>

### <span data-ttu-id="eafd4-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="eafd4-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eafd4-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="eafd4-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eafd4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="eafd4-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eafd4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eafd4-108">DESCRIPTION</span></span>
<span data-ttu-id="eafd4-109">O cmdlet **Get-AzDeploymentManagerStep** Obtém uma etapa e retorna um objeto que representa essa etapa.</span><span class="sxs-lookup"><span data-stu-id="eafd4-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="eafd4-110">Especifique a etapa pelo nome e pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eafd4-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="eafd4-111">Como alternativa, você pode fornecer o objeto Step ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="eafd4-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="eafd4-112">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações à fonte de artefatos usando o cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="eafd4-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="eafd4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eafd4-113">EXAMPLES</span></span>

### <span data-ttu-id="eafd4-114">Exemplo 1: obter uma etapa</span><span class="sxs-lookup"><span data-stu-id="eafd4-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="eafd4-115">Esse comando obtém uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eafd4-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="eafd4-116">Exemplo 2: obter uma etapa usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="eafd4-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="eafd4-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eafd4-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="eafd4-118">Esse comando obtém uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eafd4-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="eafd4-119">Exemplo 3: obter uma etapa usando um objeto retornado por New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="eafd4-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="eafd4-120">Esse comando obtém uma etapa cujo nome e o meu nome do elemento de Resource correspondem às propriedades Name e ResourceGroupName do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="eafd4-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="eafd4-121">OS</span><span class="sxs-lookup"><span data-stu-id="eafd4-121">PARAMETERS</span></span>

### <span data-ttu-id="eafd4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafd4-122">-DefaultProfile</span></span>
<span data-ttu-id="eafd4-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eafd4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eafd4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eafd4-124">-InputObject</span></span>
<span data-ttu-id="eafd4-125">O objeto de recurso etapa.</span><span class="sxs-lookup"><span data-stu-id="eafd4-125">The step resource object.</span></span>

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

### <span data-ttu-id="eafd4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="eafd4-126">-Name</span></span>
<span data-ttu-id="eafd4-127">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="eafd4-127">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafd4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eafd4-128">-ResourceGroupName</span></span>
<span data-ttu-id="eafd4-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eafd4-129">The resource group.</span></span>

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

### <span data-ttu-id="eafd4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eafd4-130">-ResourceId</span></span>
<span data-ttu-id="eafd4-131">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="eafd4-131">The resource identifier.</span></span>

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

### <span data-ttu-id="eafd4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafd4-132">CommonParameters</span></span>
<span data-ttu-id="eafd4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eafd4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafd4-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafd4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafd4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eafd4-135">INPUTS</span></span>

### <span data-ttu-id="eafd4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="eafd4-136">System.String</span></span>

### <span data-ttu-id="eafd4-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="eafd4-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="eafd4-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eafd4-138">OUTPUTS</span></span>

### <span data-ttu-id="eafd4-139">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="eafd4-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="eafd4-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eafd4-140">NOTES</span></span>

## <span data-ttu-id="eafd4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eafd4-141">RELATED LINKS</span></span>
