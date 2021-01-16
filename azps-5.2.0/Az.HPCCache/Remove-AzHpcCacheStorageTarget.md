---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263062"
---
# <span data-ttu-id="e68a1-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="e68a1-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="e68a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e68a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e68a1-103">Remove um destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e68a1-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="e68a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e68a1-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e68a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e68a1-105">DESCRIPTION</span></span>
<span data-ttu-id="e68a1-106">O cmdlet **Remove-AzHpcCacheStorageTarget** remove um destino de armazenamento do cache do Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="e68a1-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="e68a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e68a1-107">EXAMPLES</span></span>

### <span data-ttu-id="e68a1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e68a1-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="e68a1-109">OS</span><span class="sxs-lookup"><span data-stu-id="e68a1-109">PARAMETERS</span></span>

### <span data-ttu-id="e68a1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e68a1-110">-AsJob</span></span>
<span data-ttu-id="e68a1-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e68a1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e68a1-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="e68a1-112">-CacheName</span></span>
<span data-ttu-id="e68a1-113">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="e68a1-113">Name of cache.</span></span>

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

### <span data-ttu-id="e68a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68a1-114">-DefaultProfile</span></span>
<span data-ttu-id="e68a1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e68a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e68a1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e68a1-116">-Force</span></span>
<span data-ttu-id="e68a1-117">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="e68a1-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e68a1-118">Por padrão, esse cmdlet solicita que você confirme se deseja remover o destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e68a1-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="e68a1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e68a1-119">-Name</span></span>
<span data-ttu-id="e68a1-120">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e68a1-120">Name of storage target.</span></span>

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

### <span data-ttu-id="e68a1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e68a1-121">-PassThru</span></span>
<span data-ttu-id="e68a1-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e68a1-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e68a1-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e68a1-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e68a1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e68a1-124">-ResourceGroupName</span></span>
<span data-ttu-id="e68a1-125">Nome do grupo de recursos sob o qual você deseja remover o destino de armazenamento do cache.</span><span class="sxs-lookup"><span data-stu-id="e68a1-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="e68a1-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e68a1-126">-Confirm</span></span>
<span data-ttu-id="e68a1-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e68a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e68a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e68a1-128">-WhatIf</span></span>
<span data-ttu-id="e68a1-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e68a1-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e68a1-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e68a1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e68a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68a1-131">CommonParameters</span></span>
<span data-ttu-id="e68a1-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e68a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68a1-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e68a1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68a1-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e68a1-134">INPUTS</span></span>

### <span data-ttu-id="e68a1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e68a1-135">System.String</span></span>

## <span data-ttu-id="e68a1-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e68a1-136">OUTPUTS</span></span>

## <span data-ttu-id="e68a1-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e68a1-137">NOTES</span></span>

## <span data-ttu-id="e68a1-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e68a1-138">RELATED LINKS</span></span>
