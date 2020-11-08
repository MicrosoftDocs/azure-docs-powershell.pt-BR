---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112220"
---
# <span data-ttu-id="d928e-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d928e-101">New-AzHpcCache</span></span>

## <span data-ttu-id="d928e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d928e-102">SYNOPSIS</span></span>
<span data-ttu-id="d928e-103">Cria um cache HPC.</span><span class="sxs-lookup"><span data-stu-id="d928e-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="d928e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d928e-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d928e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d928e-105">DESCRIPTION</span></span>
<span data-ttu-id="d928e-106">O cmdlet **New-AzHpcCache** cria um cache do Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="d928e-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="d928e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d928e-107">EXAMPLES</span></span>

### <span data-ttu-id="d928e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d928e-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="d928e-109">OS</span><span class="sxs-lookup"><span data-stu-id="d928e-109">PARAMETERS</span></span>

### <span data-ttu-id="d928e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d928e-110">-AsJob</span></span>
<span data-ttu-id="d928e-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d928e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d928e-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="d928e-112">-CacheSize</span></span>
<span data-ttu-id="d928e-113">Ches.</span><span class="sxs-lookup"><span data-stu-id="d928e-113">CacheSize.</span></span>

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

### <span data-ttu-id="d928e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d928e-114">-DefaultProfile</span></span>
<span data-ttu-id="d928e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d928e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d928e-116">-Local</span><span class="sxs-lookup"><span data-stu-id="d928e-116">-Location</span></span>
<span data-ttu-id="d928e-117">Ponto.</span><span class="sxs-lookup"><span data-stu-id="d928e-117">Location.</span></span>

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

### <span data-ttu-id="d928e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d928e-118">-Name</span></span>
<span data-ttu-id="d928e-119">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="d928e-119">Name of cache.</span></span>

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

### <span data-ttu-id="d928e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d928e-120">-ResourceGroupName</span></span>
<span data-ttu-id="d928e-121">Nome do grupo de recursos sob o qual você deseja criar o cache.</span><span class="sxs-lookup"><span data-stu-id="d928e-121">Name of resource group under which you want to create cache.</span></span>

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

### <span data-ttu-id="d928e-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="d928e-122">-Sku</span></span>
<span data-ttu-id="d928e-123">SKU.</span><span class="sxs-lookup"><span data-stu-id="d928e-123">Sku.</span></span>

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

### <span data-ttu-id="d928e-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="d928e-124">-SubnetUri</span></span>
<span data-ttu-id="d928e-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="d928e-125">SubnetURI.</span></span>

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

### <span data-ttu-id="d928e-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="d928e-126">-Tag</span></span>
<span data-ttu-id="d928e-127">As marcas a serem associadas ao cache do HPC.</span><span class="sxs-lookup"><span data-stu-id="d928e-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="d928e-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d928e-128">-Confirm</span></span>
<span data-ttu-id="d928e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d928e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d928e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d928e-130">-WhatIf</span></span>
<span data-ttu-id="d928e-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d928e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d928e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d928e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d928e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d928e-133">CommonParameters</span></span>
<span data-ttu-id="d928e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d928e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d928e-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d928e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d928e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d928e-136">INPUTS</span></span>

### <span data-ttu-id="d928e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d928e-137">System.String</span></span>

### <span data-ttu-id="d928e-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d928e-138">System.Int32</span></span>

## <span data-ttu-id="d928e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d928e-139">OUTPUTS</span></span>

### <span data-ttu-id="d928e-140">Microsoft. Azure. PowerShell. cmdlets. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="d928e-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="d928e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d928e-141">NOTES</span></span>

## <span data-ttu-id="d928e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d928e-142">RELATED LINKS</span></span>
