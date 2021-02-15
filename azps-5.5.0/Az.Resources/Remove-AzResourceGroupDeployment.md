---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116209"
---
# <span data-ttu-id="55511-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55511-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="55511-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55511-102">SYNOPSIS</span></span>
<span data-ttu-id="55511-103">Remove uma implantação de grupo de recursos e quaisquer operações associadas.</span><span class="sxs-lookup"><span data-stu-id="55511-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="55511-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55511-104">SYNTAX</span></span>

### <span data-ttu-id="55511-105">RemoveByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="55511-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55511-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="55511-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55511-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="55511-107">DESCRIPTION</span></span>

<span data-ttu-id="55511-108">O cmdlet **Remove-AzResourceGroupDeployment** remove uma implantação de grupo de recursos do Azure e quaisquer operações associadas.</span><span class="sxs-lookup"><span data-stu-id="55511-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="55511-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55511-109">EXAMPLES</span></span>

### <span data-ttu-id="55511-110">Exemplo 1: remove uma implantação de grupo de recursos com ResourceId</span><span class="sxs-lookup"><span data-stu-id="55511-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="55511-111">Esse comando remove uma implantação de grupo de recursos com a ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="55511-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="55511-112">A remoção bem-sucedida retorna verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="55511-112">Successful removal returns true.</span></span>

### <span data-ttu-id="55511-113">Exemplo 2: remove uma implantação de grupo de recursos com ResourceGroupName e ResourceName</span><span class="sxs-lookup"><span data-stu-id="55511-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="55511-114">Esse comando remove uma implantação de grupo de recursos com o ResourceGroupName e o ResourceName fornecidos.</span><span class="sxs-lookup"><span data-stu-id="55511-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="55511-115">A remoção bem-sucedida retorna verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="55511-115">Successful removal returns true.</span></span>

## <span data-ttu-id="55511-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55511-116">PARAMETERS</span></span>

### <span data-ttu-id="55511-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55511-117">-DefaultProfile</span></span>
<span data-ttu-id="55511-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="55511-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55511-119">-ID</span><span class="sxs-lookup"><span data-stu-id="55511-119">-Id</span></span>
<span data-ttu-id="55511-120">Especifica a ID da implantação do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="55511-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="55511-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="55511-121">-Name</span></span>
<span data-ttu-id="55511-122">Especifica o nome da implantação do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="55511-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="55511-123">-Pré-</span><span class="sxs-lookup"><span data-stu-id="55511-123">-Pre</span></span>
<span data-ttu-id="55511-124">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="55511-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="55511-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55511-125">-ResourceGroupName</span></span>
<span data-ttu-id="55511-126">Especifica o nome do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="55511-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="55511-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="55511-127">-Confirm</span></span>
<span data-ttu-id="55511-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55511-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55511-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55511-129">-WhatIf</span></span>
<span data-ttu-id="55511-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="55511-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55511-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55511-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55511-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55511-132">CommonParameters</span></span>
<span data-ttu-id="55511-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55511-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55511-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55511-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55511-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="55511-135">INPUTS</span></span>

### <span data-ttu-id="55511-136">System.String</span><span class="sxs-lookup"><span data-stu-id="55511-136">System.String</span></span>

## <span data-ttu-id="55511-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="55511-137">OUTPUTS</span></span>

### <span data-ttu-id="55511-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="55511-138">System.Boolean</span></span>

## <span data-ttu-id="55511-139">Notas</span><span class="sxs-lookup"><span data-stu-id="55511-139">NOTES</span></span>

## <span data-ttu-id="55511-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55511-140">RELATED LINKS</span></span>

[<span data-ttu-id="55511-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55511-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="55511-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55511-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="55511-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55511-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="55511-144">Teste-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="55511-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


