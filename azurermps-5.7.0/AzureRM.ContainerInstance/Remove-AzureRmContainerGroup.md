---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: 80343713c9bf7a0e34a1d9a3b3b75825cbb97a12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440489"
---
# <span data-ttu-id="6835c-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="6835c-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="6835c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6835c-102">SYNOPSIS</span></span>
<span data-ttu-id="6835c-103">Remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="6835c-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6835c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6835c-104">SYNTAX</span></span>

### <span data-ttu-id="6835c-105">RemoveContainerGroupByResourceGroupAndNameParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6835c-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6835c-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="6835c-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6835c-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="6835c-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6835c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6835c-108">DESCRIPTION</span></span>
<span data-ttu-id="6835c-109">O cmdlet **Remove-AzureRmContainerGroup** remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="6835c-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="6835c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6835c-110">EXAMPLES</span></span>

### <span data-ttu-id="6835c-111">Exemplo 1: Remove um grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="6835c-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="6835c-112">Esse comando Remove o grupo de contêineres especificado.</span><span class="sxs-lookup"><span data-stu-id="6835c-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="6835c-113">Exemplo 2: Remove um grupo de contêineres por tubulação</span><span class="sxs-lookup"><span data-stu-id="6835c-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="6835c-114">Esse comando Remove um grupo de contêineres por tubulação.</span><span class="sxs-lookup"><span data-stu-id="6835c-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="6835c-115">Exemplo 3: Remove um grupo de contêineres por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6835c-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="6835c-116">Esse comando Remove um grupo de contêineres por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6835c-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="6835c-117">OS</span><span class="sxs-lookup"><span data-stu-id="6835c-117">PARAMETERS</span></span>

### <span data-ttu-id="6835c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6835c-118">-DefaultProfile</span></span>
<span data-ttu-id="6835c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6835c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6835c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6835c-120">-InputObject</span></span>
<span data-ttu-id="6835c-121">O grupo de contêineres a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6835c-121">The container group to remove.</span></span>

```yaml
Type: PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6835c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6835c-122">-Name</span></span>
<span data-ttu-id="6835c-123">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="6835c-123">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6835c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6835c-124">-PassThru</span></span>
<span data-ttu-id="6835c-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="6835c-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6835c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6835c-126">-ResourceGroupName</span></span>
<span data-ttu-id="6835c-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6835c-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6835c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6835c-128">-ResourceId</span></span>
<span data-ttu-id="6835c-129">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6835c-129">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6835c-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6835c-130">-Confirm</span></span>
<span data-ttu-id="6835c-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6835c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6835c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6835c-132">-WhatIf</span></span>
<span data-ttu-id="6835c-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6835c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6835c-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6835c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6835c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6835c-135">CommonParameters</span></span>
<span data-ttu-id="6835c-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6835c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6835c-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6835c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6835c-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6835c-138">INPUTS</span></span>

### <span data-ttu-id="6835c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6835c-139">System.String</span></span>
<span data-ttu-id="6835c-140">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="6835c-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="6835c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6835c-141">OUTPUTS</span></span>

### <span data-ttu-id="6835c-142">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="6835c-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="6835c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6835c-143">NOTES</span></span>

## <span data-ttu-id="6835c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6835c-144">RELATED LINKS</span></span>
