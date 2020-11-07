---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941769"
---
# <span data-ttu-id="f8dc3-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8dc3-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="f8dc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f8dc3-103">Remove uma implantação em um grupo de gerenciamento e quaisquer operações associadas</span><span class="sxs-lookup"><span data-stu-id="f8dc3-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="f8dc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8dc3-104">SYNTAX</span></span>

### <span data-ttu-id="f8dc3-105">RemoveByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f8dc3-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8dc3-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f8dc3-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8dc3-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f8dc3-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8dc3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8dc3-108">DESCRIPTION</span></span>
<span data-ttu-id="f8dc3-109">O cmdlet **Remove-AzManagementGroupDeployment** remove uma implantação do Azure em um grupo de gerenciamento e quaisquer operações associadas.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="f8dc3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8dc3-110">EXAMPLES</span></span>

### <span data-ttu-id="f8dc3-111">Exemplo 1: remover uma implantação com um nome específico</span><span class="sxs-lookup"><span data-stu-id="f8dc3-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="f8dc3-112">Esse comando Remove a implantação "RolesDeployment" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="f8dc3-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="f8dc3-113">Exemplo 2: obter uma implantação e removê-la</span><span class="sxs-lookup"><span data-stu-id="f8dc3-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="f8dc3-114">Esse comando obtém a implantação "RolesDeployment" no grupo de gerenciamento "myMG" e a remove.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="f8dc3-115">OS</span><span class="sxs-lookup"><span data-stu-id="f8dc3-115">PARAMETERS</span></span>

### <span data-ttu-id="f8dc3-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f8dc3-116">-ApiVersion</span></span>
<span data-ttu-id="f8dc3-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f8dc3-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f8dc3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8dc3-119">-AsJob</span></span>
<span data-ttu-id="f8dc3-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f8dc3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8dc3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8dc3-121">-DefaultProfile</span></span>
<span data-ttu-id="f8dc3-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8dc3-123">-ID</span><span class="sxs-lookup"><span data-stu-id="f8dc3-123">-Id</span></span>
<span data-ttu-id="f8dc3-124">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f8dc3-125">exemplo:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f8dc3-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8dc3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8dc3-126">-InputObject</span></span>
<span data-ttu-id="f8dc3-127">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8dc3-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f8dc3-128">-ManagementGroupId</span></span>
<span data-ttu-id="f8dc3-129">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8dc3-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8dc3-130">-Name</span></span>
<span data-ttu-id="f8dc3-131">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8dc3-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8dc3-132">-PassThru</span></span>
<span data-ttu-id="f8dc3-133">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="f8dc3-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f8dc3-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="f8dc3-134">-Pre</span></span>
<span data-ttu-id="f8dc3-135">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f8dc3-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f8dc3-136">-Confirm</span></span>
<span data-ttu-id="f8dc3-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8dc3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8dc3-138">-WhatIf</span></span>
<span data-ttu-id="f8dc3-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8dc3-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8dc3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8dc3-141">CommonParameters</span></span>
<span data-ttu-id="f8dc3-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8dc3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8dc3-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8dc3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8dc3-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8dc3-144">INPUTS</span></span>

### <span data-ttu-id="f8dc3-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="f8dc3-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f8dc3-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8dc3-146">OUTPUTS</span></span>

### <span data-ttu-id="f8dc3-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8dc3-147">System.Boolean</span></span>

## <span data-ttu-id="f8dc3-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8dc3-148">NOTES</span></span>

## <span data-ttu-id="f8dc3-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8dc3-149">RELATED LINKS</span></span>
