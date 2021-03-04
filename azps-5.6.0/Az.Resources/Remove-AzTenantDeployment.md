---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: f995050e86189c1b84652895ad0434403c4e86d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888811"
---
# <span data-ttu-id="57618-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="57618-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="57618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57618-102">SYNOPSIS</span></span>
<span data-ttu-id="57618-103">Remove uma implantação no escopo do locatário e quaisquer operações associadas</span><span class="sxs-lookup"><span data-stu-id="57618-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="57618-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57618-104">SYNTAX</span></span>

### <span data-ttu-id="57618-105">RemoveByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57618-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57618-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="57618-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57618-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="57618-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57618-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57618-108">DESCRIPTION</span></span>
<span data-ttu-id="57618-109">O cmdlet **Remove-AzTenantDeployment** remove uma implantação do Azure no escopo do locatário atual e em qualquer operação associada.</span><span class="sxs-lookup"><span data-stu-id="57618-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="57618-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57618-110">EXAMPLES</span></span>

### <span data-ttu-id="57618-111">Exemplo 1: Remover uma implantação com um determinado nome</span><span class="sxs-lookup"><span data-stu-id="57618-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="57618-112">Este comando remove a implantação "RolesDeployment" no escopo de locatário atual.</span><span class="sxs-lookup"><span data-stu-id="57618-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="57618-113">Exemplo 2: Obter uma implantação e removê-la</span><span class="sxs-lookup"><span data-stu-id="57618-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="57618-114">Este comando obtém a implantação "RolesDeployment" no escopo de locatário atual e o remove.</span><span class="sxs-lookup"><span data-stu-id="57618-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="57618-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57618-115">PARAMETERS</span></span>

### <span data-ttu-id="57618-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57618-116">-AsJob</span></span>
<span data-ttu-id="57618-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="57618-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57618-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57618-118">-DefaultProfile</span></span>
<span data-ttu-id="57618-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57618-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57618-120">-Id</span><span class="sxs-lookup"><span data-stu-id="57618-120">-Id</span></span>
<span data-ttu-id="57618-121">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="57618-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="57618-122">exemplo: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="57618-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="57618-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57618-123">-InputObject</span></span>
<span data-ttu-id="57618-124">O objeto deployment.</span><span class="sxs-lookup"><span data-stu-id="57618-124">The deployment object.</span></span>

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

### <span data-ttu-id="57618-125">-Name</span><span class="sxs-lookup"><span data-stu-id="57618-125">-Name</span></span>
<span data-ttu-id="57618-126">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="57618-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="57618-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57618-127">-PassThru</span></span>
<span data-ttu-id="57618-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="57618-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="57618-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="57618-129">-Pre</span></span>
<span data-ttu-id="57618-130">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="57618-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="57618-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57618-131">-Confirm</span></span>
<span data-ttu-id="57618-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57618-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57618-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57618-133">-WhatIf</span></span>
<span data-ttu-id="57618-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57618-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57618-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57618-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57618-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57618-136">CommonParameters</span></span>
<span data-ttu-id="57618-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57618-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57618-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57618-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57618-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57618-139">INPUTS</span></span>

### <span data-ttu-id="57618-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="57618-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="57618-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57618-141">OUTPUTS</span></span>

### <span data-ttu-id="57618-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57618-142">System.Boolean</span></span>

## <span data-ttu-id="57618-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="57618-143">NOTES</span></span>

## <span data-ttu-id="57618-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57618-144">RELATED LINKS</span></span>
