---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 9aeba4d3d7b716910ddab1e63713bd6ef2bce17a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892040"
---
# <span data-ttu-id="db8e1-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="db8e1-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="db8e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="db8e1-103">Remove uma implantação e quaisquer operações associadas</span><span class="sxs-lookup"><span data-stu-id="db8e1-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="db8e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="db8e1-104">SYNTAX</span></span>

### <span data-ttu-id="db8e1-105">RemoveByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db8e1-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db8e1-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="db8e1-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db8e1-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="db8e1-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db8e1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="db8e1-108">DESCRIPTION</span></span>
<span data-ttu-id="db8e1-109">O cmdlet **Remove-AzDeployment** remove uma implantação do Azure no escopo da assinatura e em qualquer operação associada.</span><span class="sxs-lookup"><span data-stu-id="db8e1-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="db8e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db8e1-110">EXAMPLES</span></span>

### <span data-ttu-id="db8e1-111">Exemplo 1: Remover uma implantação com um determinado nome</span><span class="sxs-lookup"><span data-stu-id="db8e1-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="db8e1-112">Este comando remove a implantação "RolesDeployment" no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="db8e1-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="db8e1-113">Exemplo 2: Obter uma implantação e removê-la</span><span class="sxs-lookup"><span data-stu-id="db8e1-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="db8e1-114">Este comando obtém a implantação "RolesDeployment" no escopo de assinatura atual e o remove.</span><span class="sxs-lookup"><span data-stu-id="db8e1-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="db8e1-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="db8e1-115">PARAMETERS</span></span>

### <span data-ttu-id="db8e1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db8e1-116">-AsJob</span></span>
<span data-ttu-id="db8e1-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="db8e1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db8e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db8e1-118">-DefaultProfile</span></span>
<span data-ttu-id="db8e1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db8e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db8e1-120">-Id</span><span class="sxs-lookup"><span data-stu-id="db8e1-120">-Id</span></span>
<span data-ttu-id="db8e1-121">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="db8e1-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="db8e1-122">exemplo: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="db8e1-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db8e1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db8e1-123">-InputObject</span></span>
<span data-ttu-id="db8e1-124">O objeto deployment.</span><span class="sxs-lookup"><span data-stu-id="db8e1-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db8e1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="db8e1-125">-Name</span></span>
<span data-ttu-id="db8e1-126">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="db8e1-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db8e1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db8e1-127">-PassThru</span></span>
<span data-ttu-id="db8e1-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="db8e1-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="db8e1-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="db8e1-129">-Pre</span></span>
<span data-ttu-id="db8e1-130">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="db8e1-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="db8e1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db8e1-131">-Confirm</span></span>
<span data-ttu-id="db8e1-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db8e1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db8e1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db8e1-133">-WhatIf</span></span>
<span data-ttu-id="db8e1-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db8e1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db8e1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db8e1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db8e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db8e1-136">CommonParameters</span></span>
<span data-ttu-id="db8e1-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db8e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db8e1-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db8e1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db8e1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db8e1-139">INPUTS</span></span>

### <span data-ttu-id="db8e1-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="db8e1-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="db8e1-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="db8e1-141">OUTPUTS</span></span>

### <span data-ttu-id="db8e1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db8e1-142">System.Boolean</span></span>

## <span data-ttu-id="db8e1-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="db8e1-143">NOTES</span></span>

## <span data-ttu-id="db8e1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db8e1-144">RELATED LINKS</span></span>
