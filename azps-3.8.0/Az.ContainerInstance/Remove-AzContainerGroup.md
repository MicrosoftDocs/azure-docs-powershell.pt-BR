---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777583"
---
# <span data-ttu-id="a0131-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a0131-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="a0131-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0131-102">SYNOPSIS</span></span>
<span data-ttu-id="a0131-103">Remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="a0131-103">Removes a container group.</span></span>

## <span data-ttu-id="a0131-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0131-104">SYNTAX</span></span>

### <span data-ttu-id="a0131-105">RemoveContainerGroupByResourceGroupAndNameParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0131-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0131-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a0131-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0131-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="a0131-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0131-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0131-108">DESCRIPTION</span></span>
<span data-ttu-id="a0131-109">O cmdlet **Remove-AzContainerGroup** remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="a0131-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="a0131-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0131-110">EXAMPLES</span></span>

### <span data-ttu-id="a0131-111">Exemplo 1: Remove um grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="a0131-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="a0131-112">Esse comando Remove o grupo de contêineres especificado.</span><span class="sxs-lookup"><span data-stu-id="a0131-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="a0131-113">Exemplo 2: Remove um grupo de contêineres por tubulação</span><span class="sxs-lookup"><span data-stu-id="a0131-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="a0131-114">Esse comando Remove um grupo de contêineres por tubulação.</span><span class="sxs-lookup"><span data-stu-id="a0131-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="a0131-115">Exemplo 3: Remove um grupo de contêineres por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a0131-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="a0131-116">Esse comando Remove um grupo de contêineres por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a0131-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="a0131-117">OS</span><span class="sxs-lookup"><span data-stu-id="a0131-117">PARAMETERS</span></span>

### <span data-ttu-id="a0131-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0131-118">-DefaultProfile</span></span>
<span data-ttu-id="a0131-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0131-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0131-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0131-120">-InputObject</span></span>
<span data-ttu-id="a0131-121">O grupo de contêineres a ser removido.</span><span class="sxs-lookup"><span data-stu-id="a0131-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0131-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0131-122">-Name</span></span>
<span data-ttu-id="a0131-123">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="a0131-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0131-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0131-124">-PassThru</span></span>
<span data-ttu-id="a0131-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="a0131-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a0131-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0131-126">-ResourceGroupName</span></span>
<span data-ttu-id="a0131-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0131-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0131-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0131-128">-ResourceId</span></span>
<span data-ttu-id="a0131-129">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a0131-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0131-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a0131-130">-Confirm</span></span>
<span data-ttu-id="a0131-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0131-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0131-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0131-132">-WhatIf</span></span>
<span data-ttu-id="a0131-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0131-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0131-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0131-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0131-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0131-135">CommonParameters</span></span>
<span data-ttu-id="a0131-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0131-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0131-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0131-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0131-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0131-138">INPUTS</span></span>

### <span data-ttu-id="a0131-139">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a0131-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="a0131-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a0131-140">System.String</span></span>

## <span data-ttu-id="a0131-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0131-141">OUTPUTS</span></span>

### <span data-ttu-id="a0131-142">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a0131-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a0131-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0131-143">NOTES</span></span>

## <span data-ttu-id="a0131-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0131-144">RELATED LINKS</span></span>
