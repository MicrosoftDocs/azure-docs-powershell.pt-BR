---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427209"
---
# <span data-ttu-id="514d9-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="514d9-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="514d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="514d9-102">SYNOPSIS</span></span>
<span data-ttu-id="514d9-103">Remove uma implantação em um grupo de gerenciamento e quaisquer operações associadas</span><span class="sxs-lookup"><span data-stu-id="514d9-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="514d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="514d9-104">SYNTAX</span></span>

### <span data-ttu-id="514d9-105">RemoveByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="514d9-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="514d9-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="514d9-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="514d9-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="514d9-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="514d9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="514d9-108">DESCRIPTION</span></span>
<span data-ttu-id="514d9-109">O cmdlet **Remove-AzManagementGroupDeployment** remove uma implantação do Azure em um grupo de gerenciamento e quaisquer operações associadas.</span><span class="sxs-lookup"><span data-stu-id="514d9-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="514d9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="514d9-110">EXAMPLES</span></span>

### <span data-ttu-id="514d9-111">Exemplo 1: remover uma implantação com um nome específico</span><span class="sxs-lookup"><span data-stu-id="514d9-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="514d9-112">Esse comando Remove a implantação "RolesDeployment" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="514d9-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="514d9-113">Exemplo 2: obter uma implantação e removê-la</span><span class="sxs-lookup"><span data-stu-id="514d9-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="514d9-114">Esse comando obtém a implantação "RolesDeployment" no grupo de gerenciamento "myMG" e a remove.</span><span class="sxs-lookup"><span data-stu-id="514d9-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="514d9-115">OS</span><span class="sxs-lookup"><span data-stu-id="514d9-115">PARAMETERS</span></span>

### <span data-ttu-id="514d9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="514d9-116">-AsJob</span></span>
<span data-ttu-id="514d9-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="514d9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="514d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="514d9-118">-DefaultProfile</span></span>
<span data-ttu-id="514d9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="514d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="514d9-120">-ID</span><span class="sxs-lookup"><span data-stu-id="514d9-120">-Id</span></span>
<span data-ttu-id="514d9-121">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="514d9-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="514d9-122">exemplo:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="514d9-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="514d9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="514d9-123">-InputObject</span></span>
<span data-ttu-id="514d9-124">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="514d9-124">The deployment object.</span></span>

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

### <span data-ttu-id="514d9-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="514d9-125">-ManagementGroupId</span></span>
<span data-ttu-id="514d9-126">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="514d9-126">The management group id.</span></span>

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

### <span data-ttu-id="514d9-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="514d9-127">-Name</span></span>
<span data-ttu-id="514d9-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="514d9-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="514d9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="514d9-129">-PassThru</span></span>
<span data-ttu-id="514d9-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="514d9-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="514d9-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="514d9-131">-Pre</span></span>
<span data-ttu-id="514d9-132">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="514d9-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="514d9-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="514d9-133">-Confirm</span></span>
<span data-ttu-id="514d9-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="514d9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="514d9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="514d9-135">-WhatIf</span></span>
<span data-ttu-id="514d9-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="514d9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="514d9-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="514d9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="514d9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514d9-138">CommonParameters</span></span>
<span data-ttu-id="514d9-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="514d9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514d9-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="514d9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514d9-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="514d9-141">INPUTS</span></span>

### <span data-ttu-id="514d9-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="514d9-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="514d9-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="514d9-143">OUTPUTS</span></span>

### <span data-ttu-id="514d9-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="514d9-144">System.Boolean</span></span>

## <span data-ttu-id="514d9-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="514d9-145">NOTES</span></span>

## <span data-ttu-id="514d9-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="514d9-146">RELATED LINKS</span></span>
