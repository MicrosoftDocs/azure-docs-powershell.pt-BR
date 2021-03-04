---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 2af89bac9e748fca0719abf34bd672d2b09c3af5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887340"
---
# <span data-ttu-id="baa36-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="baa36-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="baa36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baa36-102">SYNOPSIS</span></span>
<span data-ttu-id="baa36-103">Cancelar uma implantação em execução em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="baa36-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="baa36-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="baa36-104">SYNTAX</span></span>

### <span data-ttu-id="baa36-105">StopByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="baa36-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa36-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="baa36-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa36-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="baa36-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baa36-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="baa36-108">DESCRIPTION</span></span>
<span data-ttu-id="baa36-109">O cmdlet **Stop-AzManagementGroupDeployment** cancela uma implantação iniciada, mas não concluída em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="baa36-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="baa36-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como Provisionamento, e não um estado concluído, como Provisionado ou Falha.</span><span class="sxs-lookup"><span data-stu-id="baa36-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="baa36-111">Para criar uma implantação em um grupo de gerenciamento, use New-AzManagementGroupDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baa36-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="baa36-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="baa36-112">EXAMPLES</span></span>

### <span data-ttu-id="baa36-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="baa36-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="baa36-114">Este comando cancela uma implantação em execução "deployment01" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="baa36-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="baa36-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="baa36-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="baa36-116">Este comando obtém a implantação "deployment01" no grupo de gerenciamento "myMG" e o cancela.</span><span class="sxs-lookup"><span data-stu-id="baa36-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="baa36-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="baa36-117">PARAMETERS</span></span>

### <span data-ttu-id="baa36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa36-118">-DefaultProfile</span></span>
<span data-ttu-id="baa36-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="baa36-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baa36-120">-Id</span><span class="sxs-lookup"><span data-stu-id="baa36-120">-Id</span></span>
<span data-ttu-id="baa36-121">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="baa36-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="baa36-122">exemplo: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="baa36-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa36-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baa36-123">-InputObject</span></span>
<span data-ttu-id="baa36-124">O objeto deployment.</span><span class="sxs-lookup"><span data-stu-id="baa36-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baa36-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="baa36-125">-ManagementGroupId</span></span>
<span data-ttu-id="baa36-126">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="baa36-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa36-127">-Name</span><span class="sxs-lookup"><span data-stu-id="baa36-127">-Name</span></span>
<span data-ttu-id="baa36-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="baa36-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa36-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="baa36-129">-PassThru</span></span>
<span data-ttu-id="baa36-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="baa36-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="baa36-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="baa36-131">-Pre</span></span>
<span data-ttu-id="baa36-132">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="baa36-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="baa36-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baa36-133">-Confirm</span></span>
<span data-ttu-id="baa36-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baa36-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baa36-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baa36-135">-WhatIf</span></span>
<span data-ttu-id="baa36-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="baa36-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baa36-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="baa36-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baa36-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa36-138">CommonParameters</span></span>
<span data-ttu-id="baa36-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baa36-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa36-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baa36-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa36-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baa36-141">INPUTS</span></span>

### <span data-ttu-id="baa36-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="baa36-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="baa36-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="baa36-143">OUTPUTS</span></span>

### <span data-ttu-id="baa36-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="baa36-144">System.Boolean</span></span>

## <span data-ttu-id="baa36-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="baa36-145">NOTES</span></span>

## <span data-ttu-id="baa36-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baa36-146">RELATED LINKS</span></span>
