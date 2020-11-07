---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: bfe0bad0104708e635b49f02cfb1eecd2474ea5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786373"
---
# <span data-ttu-id="6cb7d-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6cb7d-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="6cb7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb7d-103">Remove uma implantação de grupo de recursos e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cb7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cb7d-104">SYNTAX</span></span>

### <span data-ttu-id="6cb7d-105">RemoveByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6cb7d-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb7d-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6cb7d-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cb7d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cb7d-107">DESCRIPTION</span></span>
<span data-ttu-id="6cb7d-108">O cmdlet **Remove-AzureRmResourceGroupDeployment** remove uma implantação de grupo de recursos do Azure e todas as operações associadas.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="6cb7d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cb7d-109">EXAMPLES</span></span>

## <span data-ttu-id="6cb7d-110">OS</span><span class="sxs-lookup"><span data-stu-id="6cb7d-110">PARAMETERS</span></span>

### <span data-ttu-id="6cb7d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6cb7d-111">-ApiVersion</span></span>
<span data-ttu-id="6cb7d-112">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6cb7d-113">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6cb7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb7d-114">-DefaultProfile</span></span>
<span data-ttu-id="6cb7d-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6cb7d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cb7d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="6cb7d-116">-Id</span></span>
<span data-ttu-id="6cb7d-117">Especifica a ID da implantação do grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="6cb7d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cb7d-118">-Name</span></span>
<span data-ttu-id="6cb7d-119">Especifica o nome da implantação de grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb7d-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="6cb7d-120">-Pre</span></span>
<span data-ttu-id="6cb7d-121">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6cb7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="6cb7d-123">Especifica o nome do grupo de recursos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb7d-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6cb7d-124">-Confirm</span></span>
<span data-ttu-id="6cb7d-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb7d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb7d-126">-WhatIf</span></span>
<span data-ttu-id="6cb7d-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cb7d-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb7d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb7d-129">CommonParameters</span></span>
<span data-ttu-id="6cb7d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb7d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb7d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb7d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb7d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cb7d-132">INPUTS</span></span>

### <span data-ttu-id="6cb7d-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6cb7d-133">None</span></span>

## <span data-ttu-id="6cb7d-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cb7d-134">OUTPUTS</span></span>

## <span data-ttu-id="6cb7d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cb7d-135">NOTES</span></span>

## <span data-ttu-id="6cb7d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cb7d-136">RELATED LINKS</span></span>

[<span data-ttu-id="6cb7d-137">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6cb7d-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="6cb7d-138">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6cb7d-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="6cb7d-139">Parar-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6cb7d-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="6cb7d-140">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6cb7d-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


