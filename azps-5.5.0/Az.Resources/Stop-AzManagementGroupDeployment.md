---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118730"
---
# <span data-ttu-id="c472c-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c472c-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="c472c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c472c-102">SYNOPSIS</span></span>
<span data-ttu-id="c472c-103">Cancelar uma implantação em execução em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="c472c-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="c472c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c472c-104">SYNTAX</span></span>

### <span data-ttu-id="c472c-105">StopByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c472c-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c472c-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c472c-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c472c-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="c472c-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c472c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c472c-108">DESCRIPTION</span></span>
<span data-ttu-id="c472c-109">O cmdlet **Stop-AzManagementGroupDeployment** cancela uma implantação iniciada, mas não concluída em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="c472c-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="c472c-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como Provisionamento, e não um estado concluído, como Provisionado ou Falha.</span><span class="sxs-lookup"><span data-stu-id="c472c-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="c472c-111">Para criar uma implantação em um grupo de gerenciamento, use New-AzManagementGroupDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c472c-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="c472c-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c472c-112">EXAMPLES</span></span>

### <span data-ttu-id="c472c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c472c-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="c472c-114">Esse comando cancela uma "implantação01" de implantação em execução no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="c472c-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="c472c-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c472c-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="c472c-116">Esse comando obtém a "implantação01" de implantação no grupo de gerenciamento "myMG" e o cancela.</span><span class="sxs-lookup"><span data-stu-id="c472c-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="c472c-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c472c-117">PARAMETERS</span></span>

### <span data-ttu-id="c472c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c472c-118">-DefaultProfile</span></span>
<span data-ttu-id="c472c-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c472c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c472c-120">-ID</span><span class="sxs-lookup"><span data-stu-id="c472c-120">-Id</span></span>
<span data-ttu-id="c472c-121">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="c472c-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c472c-122">exemplo: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c472c-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="c472c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c472c-123">-InputObject</span></span>
<span data-ttu-id="c472c-124">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="c472c-124">The deployment object.</span></span>

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

### <span data-ttu-id="c472c-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c472c-125">-ManagementGroupId</span></span>
<span data-ttu-id="c472c-126">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="c472c-126">The management group id.</span></span>

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

### <span data-ttu-id="c472c-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="c472c-127">-Name</span></span>
<span data-ttu-id="c472c-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="c472c-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="c472c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c472c-129">-PassThru</span></span>
<span data-ttu-id="c472c-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="c472c-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c472c-131">-Pré-</span><span class="sxs-lookup"><span data-stu-id="c472c-131">-Pre</span></span>
<span data-ttu-id="c472c-132">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="c472c-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c472c-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c472c-133">-Confirm</span></span>
<span data-ttu-id="c472c-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c472c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c472c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c472c-135">-WhatIf</span></span>
<span data-ttu-id="c472c-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c472c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c472c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c472c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c472c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c472c-138">CommonParameters</span></span>
<span data-ttu-id="c472c-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c472c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c472c-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c472c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c472c-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="c472c-141">INPUTS</span></span>

### <span data-ttu-id="c472c-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c472c-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c472c-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="c472c-143">OUTPUTS</span></span>

### <span data-ttu-id="c472c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c472c-144">System.Boolean</span></span>

## <span data-ttu-id="c472c-145">Notas</span><span class="sxs-lookup"><span data-stu-id="c472c-145">NOTES</span></span>

## <span data-ttu-id="c472c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c472c-146">RELATED LINKS</span></span>
