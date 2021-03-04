---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: e8a9c1f65c536abb3c7b3e7aa983292ccde925a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891139"
---
# <span data-ttu-id="eeef3-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="eeef3-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="eeef3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeef3-102">SYNOPSIS</span></span>
<span data-ttu-id="eeef3-103">Exclui um IpAllocation do Azure.</span><span class="sxs-lookup"><span data-stu-id="eeef3-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="eeef3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eeef3-104">SYNTAX</span></span>

### <span data-ttu-id="eeef3-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeef3-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeef3-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeef3-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeef3-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeef3-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeef3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eeef3-108">DESCRIPTION</span></span>
<span data-ttu-id="eeef3-109">O cmdlet **Remove-AzIpAllocation** exclui um IpAllocation do Azure</span><span class="sxs-lookup"><span data-stu-id="eeef3-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="eeef3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eeef3-110">EXAMPLES</span></span>

### <span data-ttu-id="eeef3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eeef3-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="eeef3-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eeef3-112">PARAMETERS</span></span>

### <span data-ttu-id="eeef3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eeef3-113">-AsJob</span></span>
<span data-ttu-id="eeef3-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="eeef3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eeef3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeef3-115">-DefaultProfile</span></span>
<span data-ttu-id="eeef3-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eeef3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeef3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="eeef3-117">-Force</span></span>
<span data-ttu-id="eeef3-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="eeef3-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eeef3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eeef3-119">-InputObject</span></span>
<span data-ttu-id="eeef3-120">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="eeef3-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeef3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eeef3-121">-Name</span></span>
<span data-ttu-id="eeef3-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="eeef3-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeef3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eeef3-123">-PassThru</span></span>
<span data-ttu-id="eeef3-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="eeef3-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eeef3-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="eeef3-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eeef3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeef3-126">-ResourceGroupName</span></span>
<span data-ttu-id="eeef3-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eeef3-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeef3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeef3-128">-ResourceId</span></span>
<span data-ttu-id="eeef3-129">ID do recurso IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="eeef3-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeef3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eeef3-130">-Confirm</span></span>
<span data-ttu-id="eeef3-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeef3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeef3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeef3-132">-WhatIf</span></span>
<span data-ttu-id="eeef3-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eeef3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeef3-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eeef3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeef3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeef3-135">CommonParameters</span></span>
<span data-ttu-id="eeef3-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeef3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeef3-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeef3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeef3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eeef3-138">INPUTS</span></span>

### <span data-ttu-id="eeef3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="eeef3-139">System.String</span></span>

## <span data-ttu-id="eeef3-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eeef3-140">OUTPUTS</span></span>

### <span data-ttu-id="eeef3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eeef3-141">System.Boolean</span></span>

## <span data-ttu-id="eeef3-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="eeef3-142">NOTES</span></span>

## <span data-ttu-id="eeef3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eeef3-143">RELATED LINKS</span></span>
