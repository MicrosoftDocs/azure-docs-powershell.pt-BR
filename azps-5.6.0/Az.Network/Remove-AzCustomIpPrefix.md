---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: d4fcdb1ad5606753980ea323137d0b77a8580ce4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888468"
---
# <span data-ttu-id="9a3af-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9a3af-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="9a3af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a3af-102">SYNOPSIS</span></span>
<span data-ttu-id="9a3af-103">Remove um CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9a3af-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="9a3af-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9a3af-104">SYNTAX</span></span>

### <span data-ttu-id="9a3af-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9a3af-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a3af-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a3af-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a3af-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a3af-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a3af-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9a3af-108">DESCRIPTION</span></span>
<span data-ttu-id="9a3af-109">O cmdlet **Remove-AzCustomIpPrefix** remove um CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="9a3af-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="9a3af-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a3af-110">EXAMPLES</span></span>

### <span data-ttu-id="9a3af-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a3af-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="9a3af-112">Remove o CustomIpPrefix com nome $prefixName do grupo de recursos $rgName</span><span class="sxs-lookup"><span data-stu-id="9a3af-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="9a3af-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9a3af-113">PARAMETERS</span></span>

### <span data-ttu-id="9a3af-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a3af-114">-AsJob</span></span>
<span data-ttu-id="9a3af-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9a3af-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a3af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a3af-116">-DefaultProfile</span></span>
<span data-ttu-id="9a3af-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a3af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a3af-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9a3af-118">-Force</span></span>
<span data-ttu-id="9a3af-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="9a3af-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9a3af-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a3af-120">-InputObject</span></span>
<span data-ttu-id="9a3af-121">Um objeto customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="9a3af-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a3af-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9a3af-122">-Name</span></span>
<span data-ttu-id="9a3af-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9a3af-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a3af-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a3af-124">-PassThru</span></span>
<span data-ttu-id="9a3af-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9a3af-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a3af-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9a3af-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a3af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a3af-127">-ResourceGroupName</span></span>
<span data-ttu-id="9a3af-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9a3af-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a3af-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a3af-129">-ResourceId</span></span>
<span data-ttu-id="9a3af-130">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9a3af-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a3af-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a3af-131">-Confirm</span></span>
<span data-ttu-id="9a3af-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a3af-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a3af-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a3af-133">-WhatIf</span></span>
<span data-ttu-id="9a3af-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a3af-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a3af-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a3af-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a3af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a3af-136">CommonParameters</span></span>
<span data-ttu-id="9a3af-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a3af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a3af-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a3af-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a3af-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a3af-139">INPUTS</span></span>

### <span data-ttu-id="9a3af-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9a3af-140">System.String</span></span>

### <span data-ttu-id="9a3af-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9a3af-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="9a3af-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9a3af-142">OUTPUTS</span></span>

### <span data-ttu-id="9a3af-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a3af-143">System.Boolean</span></span>

## <span data-ttu-id="9a3af-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="9a3af-144">NOTES</span></span>

## <span data-ttu-id="9a3af-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a3af-145">RELATED LINKS</span></span>

[<span data-ttu-id="9a3af-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9a3af-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="9a3af-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9a3af-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="9a3af-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9a3af-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)