---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112089"
---
# <span data-ttu-id="65588-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="65588-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="65588-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65588-102">SYNOPSIS</span></span>
<span data-ttu-id="65588-103">Remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="65588-103">Removes a container group.</span></span>

## <span data-ttu-id="65588-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65588-104">SYNTAX</span></span>

### <span data-ttu-id="65588-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65588-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65588-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="65588-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65588-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="65588-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65588-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="65588-108">DESCRIPTION</span></span>
<span data-ttu-id="65588-109">O **cmdlet Remove-AzContainerGroup** remove um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="65588-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="65588-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65588-110">EXAMPLES</span></span>

### <span data-ttu-id="65588-111">Exemplo 1: remove um grupo de contêineres</span><span class="sxs-lookup"><span data-stu-id="65588-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="65588-112">Esse comando remove o grupo de contêineres especificado.</span><span class="sxs-lookup"><span data-stu-id="65588-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="65588-113">Exemplo 2: remove um grupo de contêineres por piping</span><span class="sxs-lookup"><span data-stu-id="65588-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="65588-114">Esse comando remove um grupo de contêineres por piping.</span><span class="sxs-lookup"><span data-stu-id="65588-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="65588-115">Exemplo 3: remove um grupo de contêineres por ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="65588-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="65588-116">Esse comando remove um grupo de contêineres por ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="65588-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="65588-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65588-117">PARAMETERS</span></span>

### <span data-ttu-id="65588-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65588-118">-DefaultProfile</span></span>
<span data-ttu-id="65588-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="65588-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65588-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65588-120">-InputObject</span></span>
<span data-ttu-id="65588-121">O grupo de contêineres a ser removido.</span><span class="sxs-lookup"><span data-stu-id="65588-121">The container group to remove.</span></span>

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

### <span data-ttu-id="65588-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="65588-122">-Name</span></span>
<span data-ttu-id="65588-123">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="65588-123">The container group name.</span></span>

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

### <span data-ttu-id="65588-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65588-124">-PassThru</span></span>
<span data-ttu-id="65588-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="65588-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="65588-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65588-126">-ResourceGroupName</span></span>
<span data-ttu-id="65588-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65588-127">The resource group name.</span></span>

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

### <span data-ttu-id="65588-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65588-128">-ResourceId</span></span>
<span data-ttu-id="65588-129">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="65588-129">The resource id.</span></span>

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

### <span data-ttu-id="65588-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="65588-130">-Confirm</span></span>
<span data-ttu-id="65588-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65588-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65588-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65588-132">-WhatIf</span></span>
<span data-ttu-id="65588-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="65588-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65588-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65588-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65588-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65588-135">CommonParameters</span></span>
<span data-ttu-id="65588-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65588-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65588-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65588-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65588-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="65588-138">INPUTS</span></span>

### <span data-ttu-id="65588-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="65588-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="65588-140">System.String</span><span class="sxs-lookup"><span data-stu-id="65588-140">System.String</span></span>

## <span data-ttu-id="65588-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="65588-141">OUTPUTS</span></span>

### <span data-ttu-id="65588-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="65588-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="65588-143">Notas</span><span class="sxs-lookup"><span data-stu-id="65588-143">NOTES</span></span>

## <span data-ttu-id="65588-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65588-144">RELATED LINKS</span></span>
