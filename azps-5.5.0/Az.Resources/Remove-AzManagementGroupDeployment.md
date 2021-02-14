---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117184"
---
# <span data-ttu-id="ae491-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ae491-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ae491-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae491-102">SYNOPSIS</span></span>
<span data-ttu-id="ae491-103">Remove uma implantação em um grupo de gerenciamento e quaisquer operações associadas</span><span class="sxs-lookup"><span data-stu-id="ae491-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="ae491-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae491-104">SYNTAX</span></span>

### <span data-ttu-id="ae491-105">RemoveByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae491-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae491-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ae491-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae491-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ae491-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae491-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae491-108">DESCRIPTION</span></span>
<span data-ttu-id="ae491-109">O cmdlet **Remove-AzManagementGroupDeployment** remove uma implantação do Azure em um grupo de gerenciamento e quaisquer operações associadas.</span><span class="sxs-lookup"><span data-stu-id="ae491-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="ae491-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ae491-110">EXAMPLES</span></span>

### <span data-ttu-id="ae491-111">Exemplo 1: Remover uma implantação com um determinado nome</span><span class="sxs-lookup"><span data-stu-id="ae491-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="ae491-112">Esse comando remove a implantação "RolesDeployment" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="ae491-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="ae491-113">Exemplo 2: Obter uma implantação e removê-la</span><span class="sxs-lookup"><span data-stu-id="ae491-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="ae491-114">Esse comando obtém a implantação "RolesDeployment" no grupo de gerenciamento "myMG" e o remove.</span><span class="sxs-lookup"><span data-stu-id="ae491-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="ae491-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae491-115">PARAMETERS</span></span>

### <span data-ttu-id="ae491-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae491-116">-AsJob</span></span>
<span data-ttu-id="ae491-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ae491-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae491-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae491-118">-DefaultProfile</span></span>
<span data-ttu-id="ae491-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae491-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae491-120">-ID</span><span class="sxs-lookup"><span data-stu-id="ae491-120">-Id</span></span>
<span data-ttu-id="ae491-121">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="ae491-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ae491-122">exemplo: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ae491-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="ae491-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae491-123">-InputObject</span></span>
<span data-ttu-id="ae491-124">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="ae491-124">The deployment object.</span></span>

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

### <span data-ttu-id="ae491-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ae491-125">-ManagementGroupId</span></span>
<span data-ttu-id="ae491-126">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ae491-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae491-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae491-127">-Name</span></span>
<span data-ttu-id="ae491-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="ae491-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae491-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae491-129">-PassThru</span></span>
<span data-ttu-id="ae491-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="ae491-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ae491-131">-Pré-</span><span class="sxs-lookup"><span data-stu-id="ae491-131">-Pre</span></span>
<span data-ttu-id="ae491-132">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="ae491-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ae491-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ae491-133">-Confirm</span></span>
<span data-ttu-id="ae491-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae491-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae491-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae491-135">-WhatIf</span></span>
<span data-ttu-id="ae491-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ae491-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae491-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae491-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae491-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae491-138">CommonParameters</span></span>
<span data-ttu-id="ae491-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae491-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae491-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae491-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae491-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="ae491-141">INPUTS</span></span>

### <span data-ttu-id="ae491-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ae491-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ae491-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="ae491-143">OUTPUTS</span></span>

### <span data-ttu-id="ae491-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae491-144">System.Boolean</span></span>

## <span data-ttu-id="ae491-145">Notas</span><span class="sxs-lookup"><span data-stu-id="ae491-145">NOTES</span></span>

## <span data-ttu-id="ae491-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae491-146">RELATED LINKS</span></span>
