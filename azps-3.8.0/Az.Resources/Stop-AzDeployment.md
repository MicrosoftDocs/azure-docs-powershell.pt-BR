---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 366bbdf03b5fc7a23e6b71e03e1c3f1652925e7b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941764"
---
# <span data-ttu-id="5986d-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5986d-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="5986d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5986d-102">SYNOPSIS</span></span>
<span data-ttu-id="5986d-103">Cancelar uma implantação em execução</span><span class="sxs-lookup"><span data-stu-id="5986d-103">Cancel a running deployment</span></span>

## <span data-ttu-id="5986d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5986d-104">SYNTAX</span></span>

### <span data-ttu-id="5986d-105">StopByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5986d-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5986d-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5986d-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5986d-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="5986d-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5986d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5986d-108">DESCRIPTION</span></span>
<span data-ttu-id="5986d-109">O cmdlet **Stop-AzDeployment** cancela uma implantação em escopo de assinatura que foi iniciado, mas não foi concluído.</span><span class="sxs-lookup"><span data-stu-id="5986d-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="5986d-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como provisionamento, e não um estado concluído, como provisionado ou com falha.</span><span class="sxs-lookup"><span data-stu-id="5986d-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="5986d-111">Para criar uma implantação em escopo de assinatura, use o cmdlet New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="5986d-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="5986d-112">Este cmdlet interrompe apenas uma implantação em execução.</span><span class="sxs-lookup"><span data-stu-id="5986d-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="5986d-113">Use o parâmetro *Name* para interromper uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="5986d-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="5986d-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5986d-114">EXAMPLES</span></span>

### <span data-ttu-id="5986d-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5986d-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="5986d-116">Esse comando cancela uma implantação em execução "deployment01" no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="5986d-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="5986d-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5986d-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="5986d-118">Esse comando obtém a implantação "deployment01" no escopo da assinatura atual e a cancela.</span><span class="sxs-lookup"><span data-stu-id="5986d-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="5986d-119">OS</span><span class="sxs-lookup"><span data-stu-id="5986d-119">PARAMETERS</span></span>

### <span data-ttu-id="5986d-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5986d-120">-ApiVersion</span></span>
<span data-ttu-id="5986d-121">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5986d-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5986d-122">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="5986d-122">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5986d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5986d-123">-DefaultProfile</span></span>
<span data-ttu-id="5986d-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5986d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5986d-125">-ID</span><span class="sxs-lookup"><span data-stu-id="5986d-125">-Id</span></span>
<span data-ttu-id="5986d-126">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="5986d-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="5986d-127">exemplo:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="5986d-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="5986d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5986d-128">-InputObject</span></span>
<span data-ttu-id="5986d-129">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="5986d-129">The deployment object.</span></span>

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

### <span data-ttu-id="5986d-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="5986d-130">-Name</span></span>
<span data-ttu-id="5986d-131">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="5986d-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="5986d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5986d-132">-PassThru</span></span>
<span data-ttu-id="5986d-133">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="5986d-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5986d-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="5986d-134">-Pre</span></span>
<span data-ttu-id="5986d-135">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="5986d-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5986d-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5986d-136">-Confirm</span></span>
<span data-ttu-id="5986d-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5986d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5986d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5986d-138">-WhatIf</span></span>
<span data-ttu-id="5986d-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5986d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5986d-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5986d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5986d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5986d-141">CommonParameters</span></span>
<span data-ttu-id="5986d-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5986d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5986d-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5986d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5986d-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5986d-144">INPUTS</span></span>

### <span data-ttu-id="5986d-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="5986d-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5986d-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5986d-146">OUTPUTS</span></span>

### <span data-ttu-id="5986d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5986d-147">System.Boolean</span></span>

## <span data-ttu-id="5986d-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5986d-148">NOTES</span></span>

## <span data-ttu-id="5986d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5986d-149">RELATED LINKS</span></span>
