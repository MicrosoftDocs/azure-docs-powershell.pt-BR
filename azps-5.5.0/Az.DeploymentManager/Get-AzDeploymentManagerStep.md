---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115846"
---
# <span data-ttu-id="ab009-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="ab009-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="ab009-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab009-102">SYNOPSIS</span></span>
<span data-ttu-id="ab009-103">Obtém a etapa.</span><span class="sxs-lookup"><span data-stu-id="ab009-103">Gets the step.</span></span>

## <span data-ttu-id="ab009-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab009-104">SYNTAX</span></span>

### <span data-ttu-id="ab009-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ab009-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab009-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="ab009-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab009-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab009-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab009-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab009-108">DESCRIPTION</span></span>
<span data-ttu-id="ab009-109">O cmdlet **Get-AzDeploymentManagerStep** obtém uma etapa e retorna um objeto que representa essa etapa.</span><span class="sxs-lookup"><span data-stu-id="ab009-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="ab009-110">Especifique a etapa pelo nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ab009-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="ab009-111">Como alternativa, você pode fornecer o objeto Step ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ab009-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="ab009-112">Você pode modificar esse objeto localmente e, em seguida, aplicar alterações à origem do artefato usando o cmdlet Set-AzDeploymentManagerStep texto.</span><span class="sxs-lookup"><span data-stu-id="ab009-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="ab009-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab009-113">EXAMPLES</span></span>

### <span data-ttu-id="ab009-114">Exemplo 1: Obter uma etapa</span><span class="sxs-lookup"><span data-stu-id="ab009-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="ab009-115">Esse comando recebe uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ab009-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="ab009-116">Exemplo 2: Obter uma etapa usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="ab009-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="ab009-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ab009-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="ab009-118">Esse comando recebe uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ab009-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="ab009-119">Exemplo 3: Obter uma etapa usando um objeto retornado por New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="ab009-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="ab009-120">Esse comando obtém uma etapa cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos da $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ab009-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="ab009-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab009-121">PARAMETERS</span></span>

### <span data-ttu-id="ab009-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab009-122">-DefaultProfile</span></span>
<span data-ttu-id="ab009-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab009-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab009-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab009-124">-InputObject</span></span>
<span data-ttu-id="ab009-125">O objeto de recurso de etapa.</span><span class="sxs-lookup"><span data-stu-id="ab009-125">The step resource object.</span></span>

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

### <span data-ttu-id="ab009-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab009-126">-Name</span></span>
<span data-ttu-id="ab009-127">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="ab009-127">The name of the step.</span></span>

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

### <span data-ttu-id="ab009-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab009-128">-ResourceGroupName</span></span>
<span data-ttu-id="ab009-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ab009-129">The resource group.</span></span>

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

### <span data-ttu-id="ab009-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab009-130">-ResourceId</span></span>
<span data-ttu-id="ab009-131">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="ab009-131">The resource identifier.</span></span>

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

### <span data-ttu-id="ab009-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab009-132">CommonParameters</span></span>
<span data-ttu-id="ab009-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab009-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab009-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab009-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab009-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="ab009-135">INPUTS</span></span>

### <span data-ttu-id="ab009-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ab009-136">System.String</span></span>

### <span data-ttu-id="ab009-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ab009-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ab009-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="ab009-138">OUTPUTS</span></span>

### <span data-ttu-id="ab009-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ab009-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ab009-140">Notas</span><span class="sxs-lookup"><span data-stu-id="ab009-140">NOTES</span></span>

## <span data-ttu-id="ab009-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab009-141">RELATED LINKS</span></span>
