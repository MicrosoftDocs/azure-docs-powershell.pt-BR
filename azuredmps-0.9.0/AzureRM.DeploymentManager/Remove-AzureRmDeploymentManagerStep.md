---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425724"
---
# <span data-ttu-id="eb979-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="eb979-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="eb979-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb979-102">SYNOPSIS</span></span>
<span data-ttu-id="eb979-103">Exclui uma etapa.</span><span class="sxs-lookup"><span data-stu-id="eb979-103">Deletes a step.</span></span>

## <span data-ttu-id="eb979-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb979-104">SYNTAX</span></span>

### <span data-ttu-id="eb979-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb979-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb979-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="eb979-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb979-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="eb979-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb979-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb979-108">DESCRIPTION</span></span>
<span data-ttu-id="eb979-109">O cmdlet **Remove-AzureRmDeploymentManagerStep** exclui uma etapa.</span><span class="sxs-lookup"><span data-stu-id="eb979-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="eb979-110">Especifique a etapa pelo nome e pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb979-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="eb979-111">Como alternativa, você pode fornecer o objeto Step ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="eb979-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="eb979-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb979-112">EXAMPLES</span></span>
### <span data-ttu-id="eb979-113">Exemplo 1: remover uma etapa</span><span class="sxs-lookup"><span data-stu-id="eb979-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="eb979-114">Esse comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eb979-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="eb979-115">Exemplo 2: remover uma etapa usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="eb979-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="eb979-116">Esse comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eb979-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="eb979-117">Exemplo 3: remover uma etapa usando um objeto retornado por New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="eb979-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="eb979-118">Esse comando exclui uma etapa cujo nome e o nome da fonte de renome coincidem com as propriedades Name e ResourceGroupName do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="eb979-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="eb979-119">OS</span><span class="sxs-lookup"><span data-stu-id="eb979-119">PARAMETERS</span></span>

### <span data-ttu-id="eb979-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb979-120">-DefaultProfile</span></span>
<span data-ttu-id="eb979-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb979-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb979-122">-Force</span><span class="sxs-lookup"><span data-stu-id="eb979-122">-Force</span></span>
<span data-ttu-id="eb979-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="eb979-123">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb979-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb979-124">-Name</span></span>
<span data-ttu-id="eb979-125">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="eb979-125">The name of the step.</span></span>

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

### <span data-ttu-id="eb979-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb979-126">-PassThru</span></span>
<span data-ttu-id="eb979-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="eb979-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb979-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb979-128">-ResourceGroupName</span></span>
<span data-ttu-id="eb979-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb979-129">The resource group.</span></span>

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

### <span data-ttu-id="eb979-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb979-130">-ResourceId</span></span>
<span data-ttu-id="eb979-131">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="eb979-131">The resource identifier.</span></span>

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

### <span data-ttu-id="eb979-132">-Etapa</span><span class="sxs-lookup"><span data-stu-id="eb979-132">-Step</span></span>
<span data-ttu-id="eb979-133">A etapa a ser removida.</span><span class="sxs-lookup"><span data-stu-id="eb979-133">The step to be removed.</span></span>

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

### <span data-ttu-id="eb979-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eb979-134">-Confirm</span></span>
<span data-ttu-id="eb979-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb979-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb979-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb979-136">-WhatIf</span></span>
<span data-ttu-id="eb979-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eb979-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb979-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb979-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb979-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb979-139">CommonParameters</span></span>
<span data-ttu-id="eb979-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb979-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="eb979-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb979-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb979-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb979-142">INPUTS</span></span>

### <span data-ttu-id="eb979-143">System. String</span><span class="sxs-lookup"><span data-stu-id="eb979-143">System.String</span></span>

### <span data-ttu-id="eb979-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="eb979-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="eb979-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb979-145">OUTPUTS</span></span>

### <span data-ttu-id="eb979-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb979-146">System.Boolean</span></span>

## <span data-ttu-id="eb979-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb979-147">NOTES</span></span>

## <span data-ttu-id="eb979-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb979-148">RELATED LINKS</span></span>
