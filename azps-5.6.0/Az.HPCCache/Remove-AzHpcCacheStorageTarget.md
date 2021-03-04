---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 2de3856a51ce8b55d6db7a82f6e50027b60d9d87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893341"
---
# <span data-ttu-id="1043e-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="1043e-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="1043e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1043e-102">SYNOPSIS</span></span>
<span data-ttu-id="1043e-103">Remove um destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1043e-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="1043e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1043e-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1043e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1043e-105">DESCRIPTION</span></span>
<span data-ttu-id="1043e-106">O cmdlet **Remove-AzHpcCacheStorageTarget** remove um Destino de Armazenamento do Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="1043e-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="1043e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1043e-107">EXAMPLES</span></span>

### <span data-ttu-id="1043e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1043e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="1043e-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1043e-109">PARAMETERS</span></span>

### <span data-ttu-id="1043e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1043e-110">-AsJob</span></span>
<span data-ttu-id="1043e-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1043e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1043e-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="1043e-112">-CacheName</span></span>
<span data-ttu-id="1043e-113">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="1043e-113">Name of cache.</span></span>

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

### <span data-ttu-id="1043e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1043e-114">-DefaultProfile</span></span>
<span data-ttu-id="1043e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1043e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1043e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1043e-116">-Force</span></span>
<span data-ttu-id="1043e-117">Indica que o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="1043e-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="1043e-118">Por padrão, este cmdlet solicita que você confirme se deseja remover o destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1043e-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="1043e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1043e-119">-Name</span></span>
<span data-ttu-id="1043e-120">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1043e-120">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1043e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1043e-121">-PassThru</span></span>
<span data-ttu-id="1043e-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1043e-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1043e-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1043e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1043e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1043e-124">-ResourceGroupName</span></span>
<span data-ttu-id="1043e-125">Nome do grupo de recursos no qual você deseja remover o destino de armazenamento do cache.</span><span class="sxs-lookup"><span data-stu-id="1043e-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="1043e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1043e-126">-Confirm</span></span>
<span data-ttu-id="1043e-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1043e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1043e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1043e-128">-WhatIf</span></span>
<span data-ttu-id="1043e-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1043e-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1043e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1043e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1043e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1043e-131">CommonParameters</span></span>
<span data-ttu-id="1043e-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1043e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1043e-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1043e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1043e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1043e-134">INPUTS</span></span>

### <span data-ttu-id="1043e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1043e-135">System.String</span></span>

## <span data-ttu-id="1043e-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1043e-136">OUTPUTS</span></span>

## <span data-ttu-id="1043e-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="1043e-137">NOTES</span></span>

## <span data-ttu-id="1043e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1043e-138">RELATED LINKS</span></span>
