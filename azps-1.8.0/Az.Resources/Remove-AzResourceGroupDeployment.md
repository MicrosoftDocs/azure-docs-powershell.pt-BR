---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: 2cae601904b15e2508886374c1b607ed8aec4b93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599332"
---
# <span data-ttu-id="8d5cf-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d5cf-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="8d5cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5cf-103">Remove uma implantação de grupo de recursos e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="8d5cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d5cf-104">SYNTAX</span></span>

### <span data-ttu-id="8d5cf-105">RemoveByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d5cf-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d5cf-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="8d5cf-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d5cf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d5cf-107">DESCRIPTION</span></span>
<span data-ttu-id="8d5cf-108">O cmdlet **Remove-AzResourceGroupDeployment** remove uma implantação de grupo de recursos do Azure e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="8d5cf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d5cf-109">EXAMPLES</span></span>

## <span data-ttu-id="8d5cf-110">OS</span><span class="sxs-lookup"><span data-stu-id="8d5cf-110">PARAMETERS</span></span>

### <span data-ttu-id="8d5cf-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8d5cf-111">-ApiVersion</span></span>
<span data-ttu-id="8d5cf-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8d5cf-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8d5cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5cf-114">-DefaultProfile</span></span>
<span data-ttu-id="8d5cf-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8d5cf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d5cf-116">-ID</span><span class="sxs-lookup"><span data-stu-id="8d5cf-116">-Id</span></span>
<span data-ttu-id="8d5cf-117">Especifica a ID da implantação do grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="8d5cf-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d5cf-118">-Name</span></span>
<span data-ttu-id="8d5cf-119">Especifica o nome da implantação de grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="8d5cf-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="8d5cf-120">-Pre</span></span>
<span data-ttu-id="8d5cf-121">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8d5cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="8d5cf-123">Especifica o nome do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="8d5cf-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d5cf-124">-Confirm</span></span>
<span data-ttu-id="8d5cf-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d5cf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d5cf-126">-WhatIf</span></span>
<span data-ttu-id="8d5cf-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d5cf-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d5cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5cf-129">CommonParameters</span></span>
<span data-ttu-id="8d5cf-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5cf-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5cf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5cf-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d5cf-132">INPUTS</span></span>

### <span data-ttu-id="8d5cf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8d5cf-133">System.String</span></span>

## <span data-ttu-id="8d5cf-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d5cf-134">OUTPUTS</span></span>

### <span data-ttu-id="8d5cf-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d5cf-135">System.Boolean</span></span>

## <span data-ttu-id="8d5cf-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d5cf-136">NOTES</span></span>

## <span data-ttu-id="8d5cf-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d5cf-137">RELATED LINKS</span></span>

[<span data-ttu-id="8d5cf-138">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d5cf-138">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="8d5cf-139">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d5cf-139">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="8d5cf-140">Parar-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d5cf-140">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="8d5cf-141">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8d5cf-141">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


