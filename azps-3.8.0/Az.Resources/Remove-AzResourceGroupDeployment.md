---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941754"
---
# <span data-ttu-id="00c2b-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="00c2b-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="00c2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="00c2b-103">Remove uma implantação de grupo de recursos e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="00c2b-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="00c2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00c2b-104">SYNTAX</span></span>

### <span data-ttu-id="00c2b-105">RemoveByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="00c2b-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00c2b-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="00c2b-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00c2b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00c2b-107">DESCRIPTION</span></span>

<span data-ttu-id="00c2b-108">O cmdlet **Remove-AzResourceGroupDeployment** remove uma implantação de grupo de recursos do Azure e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="00c2b-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="00c2b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00c2b-109">EXAMPLES</span></span>

### <span data-ttu-id="00c2b-110">Exemplo 1: Remove uma implantação de grupo de recursos com ResourceId</span><span class="sxs-lookup"><span data-stu-id="00c2b-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="00c2b-111">Este comando Remove uma implantação de grupo de recursos com a ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="00c2b-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="00c2b-112">Remoção bem-sucedida retorna true.</span><span class="sxs-lookup"><span data-stu-id="00c2b-112">Successful removal returns true.</span></span>

### <span data-ttu-id="00c2b-113">Exemplo 2: Remove uma implantação de grupo de recursos com ResourceGroupName e resourceName</span><span class="sxs-lookup"><span data-stu-id="00c2b-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="00c2b-114">Esse comando Remove uma implantação de grupo de recursos com o ResourceGroupName e o resourcer fornecidos.</span><span class="sxs-lookup"><span data-stu-id="00c2b-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="00c2b-115">Remoção bem-sucedida retorna true.</span><span class="sxs-lookup"><span data-stu-id="00c2b-115">Successful removal returns true.</span></span>

## <span data-ttu-id="00c2b-116">OS</span><span class="sxs-lookup"><span data-stu-id="00c2b-116">PARAMETERS</span></span>

### <span data-ttu-id="00c2b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="00c2b-117">-ApiVersion</span></span>
<span data-ttu-id="00c2b-118">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="00c2b-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="00c2b-119">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="00c2b-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="00c2b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c2b-120">-DefaultProfile</span></span>
<span data-ttu-id="00c2b-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="00c2b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00c2b-122">-ID</span><span class="sxs-lookup"><span data-stu-id="00c2b-122">-Id</span></span>
<span data-ttu-id="00c2b-123">Especifica a ID da implantação do grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="00c2b-123">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="00c2b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="00c2b-124">-Name</span></span>
<span data-ttu-id="00c2b-125">Especifica o nome da implantação de grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="00c2b-125">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="00c2b-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="00c2b-126">-Pre</span></span>
<span data-ttu-id="00c2b-127">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="00c2b-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="00c2b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00c2b-128">-ResourceGroupName</span></span>
<span data-ttu-id="00c2b-129">Especifica o nome do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="00c2b-129">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="00c2b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="00c2b-130">-Confirm</span></span>
<span data-ttu-id="00c2b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00c2b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00c2b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00c2b-132">-WhatIf</span></span>
<span data-ttu-id="00c2b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00c2b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00c2b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00c2b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00c2b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c2b-135">CommonParameters</span></span>
<span data-ttu-id="00c2b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c2b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c2b-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00c2b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c2b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00c2b-138">INPUTS</span></span>

### <span data-ttu-id="00c2b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="00c2b-139">System.String</span></span>

## <span data-ttu-id="00c2b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00c2b-140">OUTPUTS</span></span>

### <span data-ttu-id="00c2b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00c2b-141">System.Boolean</span></span>

## <span data-ttu-id="00c2b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00c2b-142">NOTES</span></span>

## <span data-ttu-id="00c2b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00c2b-143">RELATED LINKS</span></span>

[<span data-ttu-id="00c2b-144">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="00c2b-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="00c2b-145">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="00c2b-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="00c2b-146">Parar-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="00c2b-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="00c2b-147">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="00c2b-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


