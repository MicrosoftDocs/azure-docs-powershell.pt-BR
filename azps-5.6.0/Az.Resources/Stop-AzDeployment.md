---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 794cc94ece2452f1fd5518d64d4071d7fa6ec326
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886855"
---
# <span data-ttu-id="7dd86-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7dd86-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="7dd86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dd86-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd86-103">Cancelar uma implantação em execução</span><span class="sxs-lookup"><span data-stu-id="7dd86-103">Cancel a running deployment</span></span>

## <span data-ttu-id="7dd86-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7dd86-104">SYNTAX</span></span>

### <span data-ttu-id="7dd86-105">StopByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7dd86-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dd86-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="7dd86-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dd86-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="7dd86-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dd86-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7dd86-108">DESCRIPTION</span></span>
<span data-ttu-id="7dd86-109">O cmdlet **Stop-AzDeployment** cancela uma implantação no escopo de assinatura iniciada, mas não concluída.</span><span class="sxs-lookup"><span data-stu-id="7dd86-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="7dd86-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como Provisionamento, e não um estado concluído, como Provisionado ou Falha.</span><span class="sxs-lookup"><span data-stu-id="7dd86-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="7dd86-111">Para criar uma implantação no escopo de assinatura, use o cmdlet New-AzDeployment de assinatura.</span><span class="sxs-lookup"><span data-stu-id="7dd86-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="7dd86-112">Este cmdlet interrompe apenas uma implantação em execução.</span><span class="sxs-lookup"><span data-stu-id="7dd86-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="7dd86-113">Use o *parâmetro Name* para interromper uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="7dd86-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="7dd86-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7dd86-114">EXAMPLES</span></span>

### <span data-ttu-id="7dd86-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7dd86-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="7dd86-116">Este comando cancela uma implantação em execução "deployment01" no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="7dd86-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="7dd86-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7dd86-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="7dd86-118">Esse comando obtém a implantação "deployment01" no escopo de assinatura atual e o cancela.</span><span class="sxs-lookup"><span data-stu-id="7dd86-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="7dd86-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7dd86-119">PARAMETERS</span></span>

### <span data-ttu-id="7dd86-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd86-120">-DefaultProfile</span></span>
<span data-ttu-id="7dd86-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd86-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dd86-122">-Id</span><span class="sxs-lookup"><span data-stu-id="7dd86-122">-Id</span></span>
<span data-ttu-id="7dd86-123">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="7dd86-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="7dd86-124">exemplo: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="7dd86-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="7dd86-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dd86-125">-InputObject</span></span>
<span data-ttu-id="7dd86-126">O objeto deployment.</span><span class="sxs-lookup"><span data-stu-id="7dd86-126">The deployment object.</span></span>

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

### <span data-ttu-id="7dd86-127">-Name</span><span class="sxs-lookup"><span data-stu-id="7dd86-127">-Name</span></span>
<span data-ttu-id="7dd86-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="7dd86-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="7dd86-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dd86-129">-PassThru</span></span>
<span data-ttu-id="7dd86-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7dd86-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7dd86-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="7dd86-131">-Pre</span></span>
<span data-ttu-id="7dd86-132">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="7dd86-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7dd86-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7dd86-133">-Confirm</span></span>
<span data-ttu-id="7dd86-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dd86-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dd86-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dd86-135">-WhatIf</span></span>
<span data-ttu-id="7dd86-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7dd86-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dd86-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7dd86-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dd86-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd86-138">CommonParameters</span></span>
<span data-ttu-id="7dd86-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd86-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd86-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dd86-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd86-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7dd86-141">INPUTS</span></span>

### <span data-ttu-id="7dd86-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7dd86-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7dd86-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7dd86-143">OUTPUTS</span></span>

### <span data-ttu-id="7dd86-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7dd86-144">System.Boolean</span></span>

## <span data-ttu-id="7dd86-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="7dd86-145">NOTES</span></span>

## <span data-ttu-id="7dd86-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dd86-146">RELATED LINKS</span></span>
