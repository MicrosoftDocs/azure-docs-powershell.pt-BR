---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116085"
---
# <span data-ttu-id="c1b62-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c1b62-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="c1b62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1b62-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b62-103">Exclui um IpAllocation do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b62-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="c1b62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1b62-104">SYNTAX</span></span>

### <span data-ttu-id="c1b62-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1b62-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1b62-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1b62-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1b62-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1b62-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1b62-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1b62-108">DESCRIPTION</span></span>
<span data-ttu-id="c1b62-109">O cmdlet **Remove-AzIpAllocation** exclui um Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="c1b62-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="c1b62-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1b62-110">EXAMPLES</span></span>

### <span data-ttu-id="c1b62-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1b62-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="c1b62-112">OS</span><span class="sxs-lookup"><span data-stu-id="c1b62-112">PARAMETERS</span></span>

### <span data-ttu-id="c1b62-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1b62-113">-AsJob</span></span>
<span data-ttu-id="c1b62-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c1b62-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1b62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b62-115">-DefaultProfile</span></span>
<span data-ttu-id="c1b62-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b62-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1b62-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c1b62-117">-Force</span></span>
<span data-ttu-id="c1b62-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c1b62-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c1b62-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1b62-119">-InputObject</span></span>
<span data-ttu-id="c1b62-120">{{Fillobject descrição da entrada}}</span><span class="sxs-lookup"><span data-stu-id="c1b62-120">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="c1b62-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1b62-121">-Name</span></span>
<span data-ttu-id="c1b62-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c1b62-122">The resource name.</span></span>

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

### <span data-ttu-id="c1b62-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1b62-123">-PassThru</span></span>
<span data-ttu-id="c1b62-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c1b62-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c1b62-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c1b62-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1b62-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b62-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1b62-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c1b62-127">The resource group name.</span></span>

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

### <span data-ttu-id="c1b62-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1b62-128">-ResourceId</span></span>
<span data-ttu-id="c1b62-129">IpAllocation ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c1b62-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="c1b62-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c1b62-130">-Confirm</span></span>
<span data-ttu-id="c1b62-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1b62-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1b62-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1b62-132">-WhatIf</span></span>
<span data-ttu-id="c1b62-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1b62-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1b62-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1b62-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1b62-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b62-135">CommonParameters</span></span>
<span data-ttu-id="c1b62-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b62-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b62-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1b62-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b62-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1b62-138">INPUTS</span></span>

### <span data-ttu-id="c1b62-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c1b62-139">System.String</span></span>

## <span data-ttu-id="c1b62-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1b62-140">OUTPUTS</span></span>

### <span data-ttu-id="c1b62-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1b62-141">System.Boolean</span></span>

## <span data-ttu-id="c1b62-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1b62-142">NOTES</span></span>

## <span data-ttu-id="c1b62-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1b62-143">RELATED LINKS</span></span>
