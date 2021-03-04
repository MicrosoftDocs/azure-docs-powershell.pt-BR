---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f345b5f03fead63a1f041e364955e68d44dd9f0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888181"
---
# <span data-ttu-id="ede52-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ede52-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="ede52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ede52-102">SYNOPSIS</span></span>
<span data-ttu-id="ede52-103">Remove uma implantação de grupo de recursos e quaisquer operações associadas.</span><span class="sxs-lookup"><span data-stu-id="ede52-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ede52-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ede52-104">SYNTAX</span></span>

### <span data-ttu-id="ede52-105">RemoveByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ede52-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ede52-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ede52-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ede52-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ede52-107">DESCRIPTION</span></span>

<span data-ttu-id="ede52-108">O cmdlet **Remove-AzResourceGroupDeployment** remove uma implantação de grupo de recursos do Azure e quaisquer operações associadas.</span><span class="sxs-lookup"><span data-stu-id="ede52-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ede52-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ede52-109">EXAMPLES</span></span>

### <span data-ttu-id="ede52-110">Exemplo 1: remove uma implantação de grupo de recursos com ResourceId</span><span class="sxs-lookup"><span data-stu-id="ede52-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="ede52-111">Este comando remove uma implantação de grupo de recursos com a ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="ede52-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ede52-112">A remoção bem-sucedida retorna true.</span><span class="sxs-lookup"><span data-stu-id="ede52-112">Successful removal returns true.</span></span>

### <span data-ttu-id="ede52-113">Exemplo 2: remove uma implantação de grupo de recursos com ResourceGroupName e ResourceName</span><span class="sxs-lookup"><span data-stu-id="ede52-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="ede52-114">Este comando remove uma implantação de grupo de recursos com ResourceGroupName e ResourceName fornecidos.</span><span class="sxs-lookup"><span data-stu-id="ede52-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="ede52-115">A remoção bem-sucedida retorna true.</span><span class="sxs-lookup"><span data-stu-id="ede52-115">Successful removal returns true.</span></span>

## <span data-ttu-id="ede52-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ede52-116">PARAMETERS</span></span>

### <span data-ttu-id="ede52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede52-117">-DefaultProfile</span></span>
<span data-ttu-id="ede52-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ede52-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ede52-119">-Id</span><span class="sxs-lookup"><span data-stu-id="ede52-119">-Id</span></span>
<span data-ttu-id="ede52-120">Especifica a ID da implantação do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ede52-120">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede52-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ede52-121">-Name</span></span>
<span data-ttu-id="ede52-122">Especifica o nome da implantação do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ede52-122">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede52-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="ede52-123">-Pre</span></span>
<span data-ttu-id="ede52-124">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="ede52-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ede52-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ede52-125">-ResourceGroupName</span></span>
<span data-ttu-id="ede52-126">Especifica o nome do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ede52-126">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede52-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ede52-127">-Confirm</span></span>
<span data-ttu-id="ede52-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ede52-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede52-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede52-129">-WhatIf</span></span>
<span data-ttu-id="ede52-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ede52-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ede52-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ede52-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede52-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede52-132">CommonParameters</span></span>
<span data-ttu-id="ede52-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ede52-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede52-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ede52-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede52-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ede52-135">INPUTS</span></span>

### <span data-ttu-id="ede52-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ede52-136">System.String</span></span>

## <span data-ttu-id="ede52-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ede52-137">OUTPUTS</span></span>

### <span data-ttu-id="ede52-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ede52-138">System.Boolean</span></span>

## <span data-ttu-id="ede52-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="ede52-139">NOTES</span></span>

## <span data-ttu-id="ede52-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ede52-140">RELATED LINKS</span></span>

[<span data-ttu-id="ede52-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ede52-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="ede52-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ede52-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="ede52-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ede52-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="ede52-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ede52-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


