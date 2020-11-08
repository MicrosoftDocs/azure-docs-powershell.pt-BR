---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125771"
---
# <span data-ttu-id="bb836-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bb836-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="bb836-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb836-102">SYNOPSIS</span></span>
<span data-ttu-id="bb836-103">Remove uma implantação de grupo de recursos e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="bb836-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="bb836-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb836-104">SYNTAX</span></span>

### <span data-ttu-id="bb836-105">RemoveByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb836-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb836-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="bb836-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb836-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb836-107">DESCRIPTION</span></span>

<span data-ttu-id="bb836-108">O cmdlet **Remove-AzResourceGroupDeployment** remove uma implantação de grupo de recursos do Azure e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="bb836-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="bb836-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb836-109">EXAMPLES</span></span>

### <span data-ttu-id="bb836-110">Exemplo 1: Remove uma implantação de grupo de recursos com ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb836-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="bb836-111">Este comando Remove uma implantação de grupo de recursos com a ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="bb836-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="bb836-112">Remoção bem-sucedida retorna true.</span><span class="sxs-lookup"><span data-stu-id="bb836-112">Successful removal returns true.</span></span>

### <span data-ttu-id="bb836-113">Exemplo 2: Remove uma implantação de grupo de recursos com ResourceGroupName e resourceName</span><span class="sxs-lookup"><span data-stu-id="bb836-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="bb836-114">Esse comando Remove uma implantação de grupo de recursos com o ResourceGroupName e o resourcer fornecidos.</span><span class="sxs-lookup"><span data-stu-id="bb836-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="bb836-115">Remoção bem-sucedida retorna true.</span><span class="sxs-lookup"><span data-stu-id="bb836-115">Successful removal returns true.</span></span>

## <span data-ttu-id="bb836-116">OS</span><span class="sxs-lookup"><span data-stu-id="bb836-116">PARAMETERS</span></span>

### <span data-ttu-id="bb836-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb836-117">-DefaultProfile</span></span>
<span data-ttu-id="bb836-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bb836-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb836-119">-ID</span><span class="sxs-lookup"><span data-stu-id="bb836-119">-Id</span></span>
<span data-ttu-id="bb836-120">Especifica a ID da implantação do grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="bb836-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="bb836-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb836-121">-Name</span></span>
<span data-ttu-id="bb836-122">Especifica o nome da implantação de grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="bb836-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="bb836-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="bb836-123">-Pre</span></span>
<span data-ttu-id="bb836-124">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="bb836-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bb836-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb836-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb836-126">Especifica o nome do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="bb836-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="bb836-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb836-127">-Confirm</span></span>
<span data-ttu-id="bb836-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb836-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb836-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb836-129">-WhatIf</span></span>
<span data-ttu-id="bb836-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb836-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb836-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb836-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb836-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb836-132">CommonParameters</span></span>
<span data-ttu-id="bb836-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb836-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb836-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb836-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb836-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb836-135">INPUTS</span></span>

### <span data-ttu-id="bb836-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bb836-136">System.String</span></span>

## <span data-ttu-id="bb836-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb836-137">OUTPUTS</span></span>

### <span data-ttu-id="bb836-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb836-138">System.Boolean</span></span>

## <span data-ttu-id="bb836-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb836-139">NOTES</span></span>

## <span data-ttu-id="bb836-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb836-140">RELATED LINKS</span></span>

[<span data-ttu-id="bb836-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bb836-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="bb836-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bb836-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="bb836-143">Parar-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bb836-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="bb836-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bb836-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


