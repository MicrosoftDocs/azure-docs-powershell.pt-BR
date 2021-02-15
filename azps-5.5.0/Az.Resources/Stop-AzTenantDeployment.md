---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111404"
---
# <span data-ttu-id="e49c7-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e49c7-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="e49c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e49c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e49c7-103">Cancelar uma implantação em execução no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="e49c7-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="e49c7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e49c7-104">SYNTAX</span></span>

### <span data-ttu-id="e49c7-105">StopByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e49c7-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e49c7-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e49c7-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e49c7-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="e49c7-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e49c7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e49c7-108">DESCRIPTION</span></span>
<span data-ttu-id="e49c7-109">O cmdlet **Stop-AzTenantDeployment** cancela uma implantação iniciada, mas não concluída no escopo atual do locatário.</span><span class="sxs-lookup"><span data-stu-id="e49c7-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="e49c7-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como Provisionamento, e não um estado concluído, como Provisionado ou Falha.</span><span class="sxs-lookup"><span data-stu-id="e49c7-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="e49c7-111">Para criar uma implantação no escopo do locatário, use o cmdlet New-AzTenantDeployment usuário.</span><span class="sxs-lookup"><span data-stu-id="e49c7-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="e49c7-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e49c7-112">EXAMPLES</span></span>

### <span data-ttu-id="e49c7-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e49c7-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="e49c7-114">Esse comando cancela uma "implantação01" de implantação em execução no escopo atual do locatário.</span><span class="sxs-lookup"><span data-stu-id="e49c7-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="e49c7-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e49c7-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="e49c7-116">Esse comando obtém a "implantação01" de implantação no escopo atual do locatário e o cancela.</span><span class="sxs-lookup"><span data-stu-id="e49c7-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="e49c7-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e49c7-117">PARAMETERS</span></span>

### <span data-ttu-id="e49c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49c7-118">-DefaultProfile</span></span>
<span data-ttu-id="e49c7-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e49c7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e49c7-120">-ID</span><span class="sxs-lookup"><span data-stu-id="e49c7-120">-Id</span></span>
<span data-ttu-id="e49c7-121">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="e49c7-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="e49c7-122">exemplo: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="e49c7-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="e49c7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e49c7-123">-InputObject</span></span>
<span data-ttu-id="e49c7-124">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="e49c7-124">The deployment object.</span></span>

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

### <span data-ttu-id="e49c7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e49c7-125">-Name</span></span>
<span data-ttu-id="e49c7-126">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="e49c7-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="e49c7-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e49c7-127">-PassThru</span></span>
<span data-ttu-id="e49c7-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="e49c7-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e49c7-129">-Pré-</span><span class="sxs-lookup"><span data-stu-id="e49c7-129">-Pre</span></span>
<span data-ttu-id="e49c7-130">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e49c7-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e49c7-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e49c7-131">-Confirm</span></span>
<span data-ttu-id="e49c7-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e49c7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e49c7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e49c7-133">-WhatIf</span></span>
<span data-ttu-id="e49c7-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e49c7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e49c7-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e49c7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e49c7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49c7-136">CommonParameters</span></span>
<span data-ttu-id="e49c7-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e49c7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49c7-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e49c7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49c7-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="e49c7-139">INPUTS</span></span>

### <span data-ttu-id="e49c7-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="e49c7-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e49c7-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="e49c7-141">OUTPUTS</span></span>

### <span data-ttu-id="e49c7-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e49c7-142">System.Boolean</span></span>

## <span data-ttu-id="e49c7-143">Notas</span><span class="sxs-lookup"><span data-stu-id="e49c7-143">NOTES</span></span>

## <span data-ttu-id="e49c7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e49c7-144">RELATED LINKS</span></span>
