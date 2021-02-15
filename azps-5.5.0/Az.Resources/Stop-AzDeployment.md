---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118731"
---
# <span data-ttu-id="982cb-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="982cb-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="982cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="982cb-102">SYNOPSIS</span></span>
<span data-ttu-id="982cb-103">Cancelar uma implantação em execução</span><span class="sxs-lookup"><span data-stu-id="982cb-103">Cancel a running deployment</span></span>

## <span data-ttu-id="982cb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="982cb-104">SYNTAX</span></span>

### <span data-ttu-id="982cb-105">StopByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="982cb-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="982cb-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="982cb-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="982cb-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="982cb-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="982cb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="982cb-108">DESCRIPTION</span></span>
<span data-ttu-id="982cb-109">O cmdlet **Stop-AzDeployment** cancela uma implantação no escopo da assinatura que foi iniciada, mas não concluída.</span><span class="sxs-lookup"><span data-stu-id="982cb-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="982cb-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como Provisionamento, e não um estado concluído, como Provisionado ou Falha.</span><span class="sxs-lookup"><span data-stu-id="982cb-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="982cb-111">Para criar uma implantação no escopo da assinatura, use o cmdlet New-AzDeployment assinatura.</span><span class="sxs-lookup"><span data-stu-id="982cb-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="982cb-112">Este cmdlet interrompe apenas uma implantação em execução.</span><span class="sxs-lookup"><span data-stu-id="982cb-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="982cb-113">Use o *parâmetro Nome* para interromper uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="982cb-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="982cb-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="982cb-114">EXAMPLES</span></span>

### <span data-ttu-id="982cb-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="982cb-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="982cb-116">Esse comando cancela uma "implantação01" de implantação em execução no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="982cb-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="982cb-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="982cb-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="982cb-118">Esse comando obtém a "implantação01" de implantação no escopo da assinatura atual e o cancela.</span><span class="sxs-lookup"><span data-stu-id="982cb-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="982cb-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="982cb-119">PARAMETERS</span></span>

### <span data-ttu-id="982cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982cb-120">-DefaultProfile</span></span>
<span data-ttu-id="982cb-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="982cb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="982cb-122">-ID</span><span class="sxs-lookup"><span data-stu-id="982cb-122">-Id</span></span>
<span data-ttu-id="982cb-123">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="982cb-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="982cb-124">exemplo: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="982cb-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="982cb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="982cb-125">-InputObject</span></span>
<span data-ttu-id="982cb-126">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="982cb-126">The deployment object.</span></span>

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

### <span data-ttu-id="982cb-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="982cb-127">-Name</span></span>
<span data-ttu-id="982cb-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="982cb-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="982cb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="982cb-129">-PassThru</span></span>
<span data-ttu-id="982cb-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="982cb-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="982cb-131">-Pré-</span><span class="sxs-lookup"><span data-stu-id="982cb-131">-Pre</span></span>
<span data-ttu-id="982cb-132">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="982cb-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="982cb-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="982cb-133">-Confirm</span></span>
<span data-ttu-id="982cb-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="982cb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="982cb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="982cb-135">-WhatIf</span></span>
<span data-ttu-id="982cb-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="982cb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="982cb-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="982cb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="982cb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982cb-138">CommonParameters</span></span>
<span data-ttu-id="982cb-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="982cb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982cb-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="982cb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982cb-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="982cb-141">INPUTS</span></span>

### <span data-ttu-id="982cb-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="982cb-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="982cb-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="982cb-143">OUTPUTS</span></span>

### <span data-ttu-id="982cb-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="982cb-144">System.Boolean</span></span>

## <span data-ttu-id="982cb-145">Notas</span><span class="sxs-lookup"><span data-stu-id="982cb-145">NOTES</span></span>

## <span data-ttu-id="982cb-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="982cb-146">RELATED LINKS</span></span>
