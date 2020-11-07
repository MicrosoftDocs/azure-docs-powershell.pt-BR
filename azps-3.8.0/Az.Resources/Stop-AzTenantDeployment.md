---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941709"
---
# <span data-ttu-id="da98e-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="da98e-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="da98e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da98e-102">SYNOPSIS</span></span>
<span data-ttu-id="da98e-103">Cancelar uma implantação em execução no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="da98e-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="da98e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da98e-104">SYNTAX</span></span>

### <span data-ttu-id="da98e-105">StopByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="da98e-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da98e-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="da98e-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da98e-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="da98e-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da98e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da98e-108">DESCRIPTION</span></span>
<span data-ttu-id="da98e-109">O cmdlet **Stop-AzTenantDeployment** cancela uma implantação que foi iniciada, mas não foi concluída no escopo do locatário atual.</span><span class="sxs-lookup"><span data-stu-id="da98e-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="da98e-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como provisionamento, e não um estado concluído, como provisionado ou com falha.</span><span class="sxs-lookup"><span data-stu-id="da98e-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="da98e-111">Para criar uma implantação no escopo do locatário, use o cmdlet New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="da98e-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="da98e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da98e-112">EXAMPLES</span></span>

### <span data-ttu-id="da98e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da98e-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="da98e-114">Esse comando cancela uma implantação em execução "deployment01" no escopo do locatário atual.</span><span class="sxs-lookup"><span data-stu-id="da98e-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="da98e-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="da98e-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="da98e-116">Esse comando obtém a implantação "deployment01" no escopo do locatário atual e a cancela.</span><span class="sxs-lookup"><span data-stu-id="da98e-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="da98e-117">OS</span><span class="sxs-lookup"><span data-stu-id="da98e-117">PARAMETERS</span></span>

### <span data-ttu-id="da98e-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="da98e-118">-ApiVersion</span></span>
<span data-ttu-id="da98e-119">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="da98e-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="da98e-120">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="da98e-120">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da98e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da98e-121">-DefaultProfile</span></span>
<span data-ttu-id="da98e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da98e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da98e-123">-ID</span><span class="sxs-lookup"><span data-stu-id="da98e-123">-Id</span></span>
<span data-ttu-id="da98e-124">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="da98e-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="da98e-125">exemplo:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="da98e-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da98e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da98e-126">-InputObject</span></span>
<span data-ttu-id="da98e-127">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="da98e-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da98e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="da98e-128">-Name</span></span>
<span data-ttu-id="da98e-129">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="da98e-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da98e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da98e-130">-PassThru</span></span>
<span data-ttu-id="da98e-131">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="da98e-131">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da98e-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="da98e-132">-Pre</span></span>
<span data-ttu-id="da98e-133">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="da98e-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da98e-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da98e-134">-Confirm</span></span>
<span data-ttu-id="da98e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da98e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da98e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da98e-136">-WhatIf</span></span>
<span data-ttu-id="da98e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da98e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da98e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da98e-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da98e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da98e-139">CommonParameters</span></span>
<span data-ttu-id="da98e-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da98e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da98e-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da98e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da98e-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da98e-142">INPUTS</span></span>

### <span data-ttu-id="da98e-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="da98e-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="da98e-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da98e-144">OUTPUTS</span></span>

### <span data-ttu-id="da98e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da98e-145">System.Boolean</span></span>

## <span data-ttu-id="da98e-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da98e-146">NOTES</span></span>

## <span data-ttu-id="da98e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da98e-147">RELATED LINKS</span></span>
