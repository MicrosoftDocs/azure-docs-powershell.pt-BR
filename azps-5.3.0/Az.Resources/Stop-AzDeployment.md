---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427196"
---
# <span data-ttu-id="0efb4-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0efb4-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="0efb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0efb4-102">SYNOPSIS</span></span>
<span data-ttu-id="0efb4-103">Cancelar uma implantação em execução</span><span class="sxs-lookup"><span data-stu-id="0efb4-103">Cancel a running deployment</span></span>

## <span data-ttu-id="0efb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0efb4-104">SYNTAX</span></span>

### <span data-ttu-id="0efb4-105">StopByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0efb4-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0efb4-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0efb4-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0efb4-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="0efb4-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0efb4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0efb4-108">DESCRIPTION</span></span>
<span data-ttu-id="0efb4-109">O cmdlet **Stop-AzDeployment** cancela uma implantação em escopo de assinatura que foi iniciado, mas não foi concluído.</span><span class="sxs-lookup"><span data-stu-id="0efb4-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="0efb4-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como provisionamento, e não um estado concluído, como provisionado ou com falha.</span><span class="sxs-lookup"><span data-stu-id="0efb4-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="0efb4-111">Para criar uma implantação em escopo de assinatura, use o cmdlet New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="0efb4-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="0efb4-112">Este cmdlet interrompe apenas uma implantação em execução.</span><span class="sxs-lookup"><span data-stu-id="0efb4-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="0efb4-113">Use o parâmetro *Name* para interromper uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="0efb4-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="0efb4-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0efb4-114">EXAMPLES</span></span>

### <span data-ttu-id="0efb4-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0efb4-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="0efb4-116">Esse comando cancela uma implantação em execução "deployment01" no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0efb4-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="0efb4-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0efb4-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="0efb4-118">Esse comando obtém a implantação "deployment01" no escopo da assinatura atual e a cancela.</span><span class="sxs-lookup"><span data-stu-id="0efb4-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="0efb4-119">OS</span><span class="sxs-lookup"><span data-stu-id="0efb4-119">PARAMETERS</span></span>

### <span data-ttu-id="0efb4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efb4-120">-DefaultProfile</span></span>
<span data-ttu-id="0efb4-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0efb4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0efb4-122">-ID</span><span class="sxs-lookup"><span data-stu-id="0efb4-122">-Id</span></span>
<span data-ttu-id="0efb4-123">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="0efb4-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0efb4-124">exemplo:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0efb4-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="0efb4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0efb4-125">-InputObject</span></span>
<span data-ttu-id="0efb4-126">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="0efb4-126">The deployment object.</span></span>

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

### <span data-ttu-id="0efb4-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="0efb4-127">-Name</span></span>
<span data-ttu-id="0efb4-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="0efb4-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="0efb4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0efb4-129">-PassThru</span></span>
<span data-ttu-id="0efb4-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="0efb4-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0efb4-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="0efb4-131">-Pre</span></span>
<span data-ttu-id="0efb4-132">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="0efb4-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0efb4-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0efb4-133">-Confirm</span></span>
<span data-ttu-id="0efb4-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0efb4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efb4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efb4-135">-WhatIf</span></span>
<span data-ttu-id="0efb4-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0efb4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0efb4-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0efb4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efb4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efb4-138">CommonParameters</span></span>
<span data-ttu-id="0efb4-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efb4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efb4-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0efb4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efb4-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0efb4-141">INPUTS</span></span>

### <span data-ttu-id="0efb4-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="0efb4-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0efb4-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0efb4-143">OUTPUTS</span></span>

### <span data-ttu-id="0efb4-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0efb4-144">System.Boolean</span></span>

## <span data-ttu-id="0efb4-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0efb4-145">NOTES</span></span>

## <span data-ttu-id="0efb4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0efb4-146">RELATED LINKS</span></span>
