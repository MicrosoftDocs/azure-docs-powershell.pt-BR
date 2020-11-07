---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: dbc5238819c6dc7a7555dd1f95ec0ba3478f2b2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772552"
---
# <span data-ttu-id="4ca8e-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4ca8e-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="4ca8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ca8e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca8e-103">Remove uma implantação e todas as operações associadas</span><span class="sxs-lookup"><span data-stu-id="4ca8e-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="4ca8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ca8e-104">SYNTAX</span></span>

### <span data-ttu-id="4ca8e-105">RemoveByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ca8e-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca8e-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4ca8e-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca8e-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ca8e-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ca8e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ca8e-108">DESCRIPTION</span></span>
<span data-ttu-id="4ca8e-109">O cmdlet **Remove-AzDeployment** remove uma implantação do Azure em escopo de assinatura e quaisquer operações associadas.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="4ca8e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ca8e-110">EXAMPLES</span></span>

### <span data-ttu-id="4ca8e-111">Exemplo 1: remover uma implantação com um nome específico</span><span class="sxs-lookup"><span data-stu-id="4ca8e-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="4ca8e-112">Esse comando Remove a implantação "RolesDeployment" no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="4ca8e-113">Exemplo 2: obter uma implantação e removê-la</span><span class="sxs-lookup"><span data-stu-id="4ca8e-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="4ca8e-114">Esse comando obtém a implantação "RolesDeployment" no escopo da assinatura atual e a remove.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="4ca8e-115">OS</span><span class="sxs-lookup"><span data-stu-id="4ca8e-115">PARAMETERS</span></span>

### <span data-ttu-id="4ca8e-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4ca8e-116">-ApiVersion</span></span>
<span data-ttu-id="4ca8e-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4ca8e-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4ca8e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ca8e-119">-AsJob</span></span>
<span data-ttu-id="4ca8e-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4ca8e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ca8e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca8e-121">-DefaultProfile</span></span>
<span data-ttu-id="4ca8e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ca8e-123">-ID</span><span class="sxs-lookup"><span data-stu-id="4ca8e-123">-Id</span></span>
<span data-ttu-id="4ca8e-124">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="4ca8e-125">exemplo:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="4ca8e-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca8e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ca8e-126">-InputObject</span></span>
<span data-ttu-id="4ca8e-127">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-127">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca8e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ca8e-128">-Name</span></span>
<span data-ttu-id="4ca8e-129">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-129">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca8e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ca8e-130">-PassThru</span></span>
<span data-ttu-id="4ca8e-131">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="4ca8e-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4ca8e-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="4ca8e-132">-Pre</span></span>
<span data-ttu-id="4ca8e-133">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4ca8e-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ca8e-134">-Confirm</span></span>
<span data-ttu-id="4ca8e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ca8e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ca8e-136">-WhatIf</span></span>
<span data-ttu-id="4ca8e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ca8e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ca8e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca8e-139">CommonParameters</span></span>
<span data-ttu-id="4ca8e-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca8e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca8e-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca8e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca8e-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ca8e-142">INPUTS</span></span>

### <span data-ttu-id="4ca8e-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="4ca8e-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4ca8e-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ca8e-144">OUTPUTS</span></span>

### <span data-ttu-id="4ca8e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ca8e-145">System.Boolean</span></span>

## <span data-ttu-id="4ca8e-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ca8e-146">NOTES</span></span>

## <span data-ttu-id="4ca8e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ca8e-147">RELATED LINKS</span></span>