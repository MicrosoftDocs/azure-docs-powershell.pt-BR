---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: e0df378cb50d7d308d5d6a9f0acf8a15466b8a11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893344"
---
# <span data-ttu-id="efb05-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="efb05-101">New-AzHpcCache</span></span>

## <span data-ttu-id="efb05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efb05-102">SYNOPSIS</span></span>
<span data-ttu-id="efb05-103">Cria um Cache HPC.</span><span class="sxs-lookup"><span data-stu-id="efb05-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="efb05-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="efb05-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efb05-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="efb05-105">DESCRIPTION</span></span>
<span data-ttu-id="efb05-106">O cmdlet **New-AzHpcCache** cria um Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="efb05-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="efb05-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efb05-107">EXAMPLES</span></span>

### <span data-ttu-id="efb05-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="efb05-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="efb05-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="efb05-109">PARAMETERS</span></span>

### <span data-ttu-id="efb05-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efb05-110">-AsJob</span></span>
<span data-ttu-id="efb05-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="efb05-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efb05-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="efb05-112">-CacheSize</span></span>
<span data-ttu-id="efb05-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="efb05-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb05-114">-DefaultProfile</span></span>
<span data-ttu-id="efb05-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="efb05-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efb05-116">-Location</span><span class="sxs-lookup"><span data-stu-id="efb05-116">-Location</span></span>
<span data-ttu-id="efb05-117">Local.</span><span class="sxs-lookup"><span data-stu-id="efb05-117">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb05-118">-Name</span><span class="sxs-lookup"><span data-stu-id="efb05-118">-Name</span></span>
<span data-ttu-id="efb05-119">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="efb05-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb05-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb05-120">-ResourceGroupName</span></span>
<span data-ttu-id="efb05-121">Nome do grupo de recursos no qual você deseja criar cache.</span><span class="sxs-lookup"><span data-stu-id="efb05-121">Name of resource group under which you want to create cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb05-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="efb05-122">-Sku</span></span>
<span data-ttu-id="efb05-123">Sku.</span><span class="sxs-lookup"><span data-stu-id="efb05-123">Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb05-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="efb05-124">-SubnetUri</span></span>
<span data-ttu-id="efb05-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="efb05-125">SubnetURI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb05-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="efb05-126">-Tag</span></span>
<span data-ttu-id="efb05-127">As marcas a associar ao Cache HPC.</span><span class="sxs-lookup"><span data-stu-id="efb05-127">The tags to associate with HPC Cache.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb05-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efb05-128">-Confirm</span></span>
<span data-ttu-id="efb05-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efb05-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb05-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb05-130">-WhatIf</span></span>
<span data-ttu-id="efb05-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="efb05-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efb05-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="efb05-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb05-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb05-133">CommonParameters</span></span>
<span data-ttu-id="efb05-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb05-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb05-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efb05-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb05-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efb05-136">INPUTS</span></span>

### <span data-ttu-id="efb05-137">System.String</span><span class="sxs-lookup"><span data-stu-id="efb05-137">System.String</span></span>

### <span data-ttu-id="efb05-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="efb05-138">System.Int32</span></span>

## <span data-ttu-id="efb05-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="efb05-139">OUTPUTS</span></span>

### <span data-ttu-id="efb05-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="efb05-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="efb05-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="efb05-141">NOTES</span></span>

## <span data-ttu-id="efb05-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efb05-142">RELATED LINKS</span></span>
