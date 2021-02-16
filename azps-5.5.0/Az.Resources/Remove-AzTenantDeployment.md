---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114020"
---
# <span data-ttu-id="52a51-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="52a51-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="52a51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52a51-102">SYNOPSIS</span></span>
<span data-ttu-id="52a51-103">Remove uma implantação no escopo do locatário e em quaisquer operações associadas</span><span class="sxs-lookup"><span data-stu-id="52a51-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="52a51-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52a51-104">SYNTAX</span></span>

### <span data-ttu-id="52a51-105">RemoveByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52a51-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a51-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="52a51-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a51-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="52a51-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a51-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="52a51-108">DESCRIPTION</span></span>
<span data-ttu-id="52a51-109">O cmdlet **Remove-AzTenantDeployment** remove uma implantação do Azure no escopo atual do locatário e em quaisquer operações associadas.</span><span class="sxs-lookup"><span data-stu-id="52a51-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="52a51-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52a51-110">EXAMPLES</span></span>

### <span data-ttu-id="52a51-111">Exemplo 1: Remover uma implantação com um determinado nome</span><span class="sxs-lookup"><span data-stu-id="52a51-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="52a51-112">Esse comando remove a implantação "RolesDeployment" no escopo atual do locatário.</span><span class="sxs-lookup"><span data-stu-id="52a51-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="52a51-113">Exemplo 2: Obter uma implantação e removê-la</span><span class="sxs-lookup"><span data-stu-id="52a51-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="52a51-114">Esse comando obtém a implantação "RolesDeployment" no escopo atual do locatário e o remove.</span><span class="sxs-lookup"><span data-stu-id="52a51-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="52a51-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52a51-115">PARAMETERS</span></span>

### <span data-ttu-id="52a51-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52a51-116">-AsJob</span></span>
<span data-ttu-id="52a51-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="52a51-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52a51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a51-118">-DefaultProfile</span></span>
<span data-ttu-id="52a51-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52a51-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a51-120">-ID</span><span class="sxs-lookup"><span data-stu-id="52a51-120">-Id</span></span>
<span data-ttu-id="52a51-121">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="52a51-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="52a51-122">exemplo: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="52a51-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="52a51-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52a51-123">-InputObject</span></span>
<span data-ttu-id="52a51-124">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="52a51-124">The deployment object.</span></span>

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

### <span data-ttu-id="52a51-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="52a51-125">-Name</span></span>
<span data-ttu-id="52a51-126">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="52a51-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="52a51-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52a51-127">-PassThru</span></span>
<span data-ttu-id="52a51-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="52a51-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="52a51-129">-Pré-</span><span class="sxs-lookup"><span data-stu-id="52a51-129">-Pre</span></span>
<span data-ttu-id="52a51-130">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="52a51-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="52a51-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="52a51-131">-Confirm</span></span>
<span data-ttu-id="52a51-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52a51-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a51-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a51-133">-WhatIf</span></span>
<span data-ttu-id="52a51-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="52a51-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a51-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52a51-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a51-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a51-136">CommonParameters</span></span>
<span data-ttu-id="52a51-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a51-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a51-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52a51-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a51-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="52a51-139">INPUTS</span></span>

### <span data-ttu-id="52a51-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="52a51-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="52a51-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="52a51-141">OUTPUTS</span></span>

### <span data-ttu-id="52a51-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52a51-142">System.Boolean</span></span>

## <span data-ttu-id="52a51-143">Notas</span><span class="sxs-lookup"><span data-stu-id="52a51-143">NOTES</span></span>

## <span data-ttu-id="52a51-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52a51-144">RELATED LINKS</span></span>
