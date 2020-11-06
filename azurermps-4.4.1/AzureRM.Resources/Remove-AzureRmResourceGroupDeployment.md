---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 84aa6f50d02f4c85de674c163565a205f2b83750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432556"
---
# <span data-ttu-id="8cf68-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8cf68-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="8cf68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cf68-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf68-103">Remove uma implantação de grupo de recursos e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="8cf68-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cf68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cf68-104">SYNTAX</span></span>

### <span data-ttu-id="8cf68-105">O parâmetro de nome de implantação definido.</span><span class="sxs-lookup"><span data-stu-id="8cf68-105">The deployment name parameter set.</span></span> <span data-ttu-id="8cf68-106">Assume</span><span class="sxs-lookup"><span data-stu-id="8cf68-106">(Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf68-107">O conjunto de parâmetros de ID de implantação.</span><span class="sxs-lookup"><span data-stu-id="8cf68-107">The deployment Id parameter set.</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf68-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8cf68-108">DESCRIPTION</span></span>
<span data-ttu-id="8cf68-109">O cmdlet **Remove-AzureRmResourceGroupDeployment** remove uma implantação de grupo de recursos do Azure e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="8cf68-109">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="8cf68-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cf68-110">EXAMPLES</span></span>

## <span data-ttu-id="8cf68-111">OS</span><span class="sxs-lookup"><span data-stu-id="8cf68-111">PARAMETERS</span></span>

### <span data-ttu-id="8cf68-112">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8cf68-112">-ApiVersion</span></span>
<span data-ttu-id="8cf68-113">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8cf68-113">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8cf68-114">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="8cf68-114">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8cf68-115">-ID</span><span class="sxs-lookup"><span data-stu-id="8cf68-115">-Id</span></span>
<span data-ttu-id="8cf68-116">Especifica a ID da implantação do grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="8cf68-116">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf68-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cf68-117">-Name</span></span>
<span data-ttu-id="8cf68-118">Especifica o nome da implantação de grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="8cf68-118">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf68-119">-Pre</span><span class="sxs-lookup"><span data-stu-id="8cf68-119">-Pre</span></span>
<span data-ttu-id="8cf68-120">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8cf68-120">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8cf68-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf68-121">-ResourceGroupName</span></span>
<span data-ttu-id="8cf68-122">Especifica o nome do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="8cf68-122">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf68-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8cf68-123">-Confirm</span></span>
<span data-ttu-id="8cf68-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf68-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf68-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf68-125">-WhatIf</span></span>
<span data-ttu-id="8cf68-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8cf68-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf68-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8cf68-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf68-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf68-128">-DefaultProfile</span></span>
<span data-ttu-id="8cf68-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf68-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf68-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf68-130">CommonParameters</span></span>
<span data-ttu-id="8cf68-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf68-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf68-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf68-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf68-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8cf68-133">INPUTS</span></span>

## <span data-ttu-id="8cf68-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8cf68-134">OUTPUTS</span></span>

### <span data-ttu-id="8cf68-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8cf68-135">System.Boolean</span></span>

## <span data-ttu-id="8cf68-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8cf68-136">NOTES</span></span>

## <span data-ttu-id="8cf68-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cf68-137">RELATED LINKS</span></span>

[<span data-ttu-id="8cf68-138">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8cf68-138">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8cf68-139">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8cf68-139">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8cf68-140">Parar-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8cf68-140">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8cf68-141">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8cf68-141">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


