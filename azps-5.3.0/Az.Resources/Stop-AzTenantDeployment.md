---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427193"
---
# <span data-ttu-id="e970f-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e970f-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="e970f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e970f-102">SYNOPSIS</span></span>
<span data-ttu-id="e970f-103">Cancelar uma implantação em execução no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="e970f-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="e970f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e970f-104">SYNTAX</span></span>

### <span data-ttu-id="e970f-105">StopByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e970f-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e970f-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e970f-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e970f-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="e970f-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e970f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e970f-108">DESCRIPTION</span></span>
<span data-ttu-id="e970f-109">O cmdlet **Stop-AzTenantDeployment** cancela uma implantação que foi iniciada, mas não foi concluída no escopo do locatário atual.</span><span class="sxs-lookup"><span data-stu-id="e970f-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="e970f-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como provisionamento, e não um estado concluído, como provisionado ou com falha.</span><span class="sxs-lookup"><span data-stu-id="e970f-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="e970f-111">Para criar uma implantação no escopo do locatário, use o cmdlet New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="e970f-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="e970f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e970f-112">EXAMPLES</span></span>

### <span data-ttu-id="e970f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e970f-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="e970f-114">Esse comando cancela uma implantação em execução "deployment01" no escopo do locatário atual.</span><span class="sxs-lookup"><span data-stu-id="e970f-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="e970f-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e970f-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="e970f-116">Esse comando obtém a implantação "deployment01" no escopo do locatário atual e a cancela.</span><span class="sxs-lookup"><span data-stu-id="e970f-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="e970f-117">OS</span><span class="sxs-lookup"><span data-stu-id="e970f-117">PARAMETERS</span></span>

### <span data-ttu-id="e970f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e970f-118">-DefaultProfile</span></span>
<span data-ttu-id="e970f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e970f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e970f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="e970f-120">-Id</span></span>
<span data-ttu-id="e970f-121">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="e970f-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="e970f-122">exemplo:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="e970f-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="e970f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e970f-123">-InputObject</span></span>
<span data-ttu-id="e970f-124">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="e970f-124">The deployment object.</span></span>

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

### <span data-ttu-id="e970f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e970f-125">-Name</span></span>
<span data-ttu-id="e970f-126">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="e970f-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e970f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e970f-127">-PassThru</span></span>
<span data-ttu-id="e970f-128">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="e970f-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e970f-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="e970f-129">-Pre</span></span>
<span data-ttu-id="e970f-130">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e970f-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e970f-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e970f-131">-Confirm</span></span>
<span data-ttu-id="e970f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e970f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e970f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e970f-133">-WhatIf</span></span>
<span data-ttu-id="e970f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e970f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e970f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e970f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e970f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e970f-136">CommonParameters</span></span>
<span data-ttu-id="e970f-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e970f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e970f-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e970f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e970f-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e970f-139">INPUTS</span></span>

### <span data-ttu-id="e970f-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="e970f-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e970f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e970f-141">OUTPUTS</span></span>

### <span data-ttu-id="e970f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e970f-142">System.Boolean</span></span>

## <span data-ttu-id="e970f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e970f-143">NOTES</span></span>

## <span data-ttu-id="e970f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e970f-144">RELATED LINKS</span></span>
