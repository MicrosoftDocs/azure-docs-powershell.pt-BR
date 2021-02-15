---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118975"
---
# <span data-ttu-id="946c8-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="946c8-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="946c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="946c8-102">SYNOPSIS</span></span>
<span data-ttu-id="946c8-103">Remove um Destino de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="946c8-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="946c8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="946c8-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="946c8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="946c8-105">DESCRIPTION</span></span>
<span data-ttu-id="946c8-106">O cmdlet **Remove-AzHpcCacheStorageTarget** remove um Destino de Armazenamento do Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="946c8-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="946c8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="946c8-107">EXAMPLES</span></span>

### <span data-ttu-id="946c8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="946c8-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="946c8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="946c8-109">PARAMETERS</span></span>

### <span data-ttu-id="946c8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="946c8-110">-AsJob</span></span>
<span data-ttu-id="946c8-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="946c8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="946c8-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="946c8-112">-CacheName</span></span>
<span data-ttu-id="946c8-113">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="946c8-113">Name of cache.</span></span>

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

### <span data-ttu-id="946c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946c8-114">-DefaultProfile</span></span>
<span data-ttu-id="946c8-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="946c8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="946c8-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="946c8-116">-Force</span></span>
<span data-ttu-id="946c8-117">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="946c8-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="946c8-118">Por padrão, esse cmdlet solicita que você confirme que deseja remover o destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="946c8-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="946c8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="946c8-119">-Name</span></span>
<span data-ttu-id="946c8-120">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="946c8-120">Name of storage target.</span></span>

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

### <span data-ttu-id="946c8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="946c8-121">-PassThru</span></span>
<span data-ttu-id="946c8-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="946c8-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="946c8-123">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="946c8-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="946c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="946c8-125">Nome do grupo de recursos no qual você deseja remover o destino de armazenamento do cache.</span><span class="sxs-lookup"><span data-stu-id="946c8-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="946c8-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="946c8-126">-Confirm</span></span>
<span data-ttu-id="946c8-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="946c8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="946c8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="946c8-128">-WhatIf</span></span>
<span data-ttu-id="946c8-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="946c8-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="946c8-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="946c8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="946c8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946c8-131">CommonParameters</span></span>
<span data-ttu-id="946c8-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="946c8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946c8-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="946c8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946c8-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="946c8-134">INPUTS</span></span>

### <span data-ttu-id="946c8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="946c8-135">System.String</span></span>

## <span data-ttu-id="946c8-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="946c8-136">OUTPUTS</span></span>

## <span data-ttu-id="946c8-137">Notas</span><span class="sxs-lookup"><span data-stu-id="946c8-137">NOTES</span></span>

## <span data-ttu-id="946c8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="946c8-138">RELATED LINKS</span></span>
