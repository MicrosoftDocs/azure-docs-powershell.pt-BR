---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261844"
---
# <span data-ttu-id="b098f-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b098f-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="b098f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b098f-102">SYNOPSIS</span></span>
<span data-ttu-id="b098f-103">Cancelar uma implantação em execução em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="b098f-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="b098f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b098f-104">SYNTAX</span></span>

### <span data-ttu-id="b098f-105">StopByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b098f-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b098f-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b098f-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b098f-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="b098f-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b098f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b098f-108">DESCRIPTION</span></span>
<span data-ttu-id="b098f-109">O cmdlet **Stop-AzManagementGroupDeployment** cancela uma implantação que foi iniciada, mas não foi concluída em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="b098f-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="b098f-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como provisionamento, e não um estado concluído, como provisionado ou com falha.</span><span class="sxs-lookup"><span data-stu-id="b098f-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="b098f-111">Para criar uma implantação em um grupo de gerenciamento, use o cmdlet New-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="b098f-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="b098f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b098f-112">EXAMPLES</span></span>

### <span data-ttu-id="b098f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b098f-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="b098f-114">Esse comando cancela uma implantação em execução "deployment01" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="b098f-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="b098f-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b098f-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="b098f-116">Este comando obtém a implantação "deployment01" no grupo de gerenciamento "myMG" e a cancela.</span><span class="sxs-lookup"><span data-stu-id="b098f-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="b098f-117">OS</span><span class="sxs-lookup"><span data-stu-id="b098f-117">PARAMETERS</span></span>

### <span data-ttu-id="b098f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b098f-118">-DefaultProfile</span></span>
<span data-ttu-id="b098f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b098f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b098f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="b098f-120">-Id</span></span>
<span data-ttu-id="b098f-121">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="b098f-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b098f-122">exemplo:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="b098f-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="b098f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b098f-123">-InputObject</span></span>
<span data-ttu-id="b098f-124">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="b098f-124">The deployment object.</span></span>

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

### <span data-ttu-id="b098f-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b098f-125">-ManagementGroupId</span></span>
<span data-ttu-id="b098f-126">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="b098f-126">The management group id.</span></span>

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

### <span data-ttu-id="b098f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="b098f-127">-Name</span></span>
<span data-ttu-id="b098f-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="b098f-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="b098f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b098f-129">-PassThru</span></span>
<span data-ttu-id="b098f-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="b098f-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b098f-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="b098f-131">-Pre</span></span>
<span data-ttu-id="b098f-132">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b098f-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b098f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b098f-133">-Confirm</span></span>
<span data-ttu-id="b098f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b098f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b098f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b098f-135">-WhatIf</span></span>
<span data-ttu-id="b098f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b098f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b098f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b098f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b098f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b098f-138">CommonParameters</span></span>
<span data-ttu-id="b098f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b098f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b098f-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b098f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b098f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b098f-141">INPUTS</span></span>

### <span data-ttu-id="b098f-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="b098f-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b098f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b098f-143">OUTPUTS</span></span>

### <span data-ttu-id="b098f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b098f-144">System.Boolean</span></span>

## <span data-ttu-id="b098f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b098f-145">NOTES</span></span>

## <span data-ttu-id="b098f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b098f-146">RELATED LINKS</span></span>
