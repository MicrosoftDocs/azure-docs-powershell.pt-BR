---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: 12bf101fb404b02fc70cbec9640f5f2bd976107c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893342"
---
# <span data-ttu-id="328b9-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="328b9-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="328b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="328b9-102">SYNOPSIS</span></span>
<span data-ttu-id="328b9-103">Remove um Cache HPC.</span><span class="sxs-lookup"><span data-stu-id="328b9-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="328b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="328b9-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="328b9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="328b9-105">DESCRIPTION</span></span>
<span data-ttu-id="328b9-106">O cmdlet **Remove-AzHpcCache** remove um Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="328b9-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="328b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="328b9-107">EXAMPLES</span></span>

### <span data-ttu-id="328b9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="328b9-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="328b9-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="328b9-109">PARAMETERS</span></span>

### <span data-ttu-id="328b9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="328b9-110">-AsJob</span></span>
<span data-ttu-id="328b9-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="328b9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="328b9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="328b9-112">-DefaultProfile</span></span>
<span data-ttu-id="328b9-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="328b9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="328b9-114">-Force</span><span class="sxs-lookup"><span data-stu-id="328b9-114">-Force</span></span>
<span data-ttu-id="328b9-115">Indica que o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="328b9-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="328b9-116">Por padrão, este cmdlet solicita que você confirme se deseja remover o cache.</span><span class="sxs-lookup"><span data-stu-id="328b9-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="328b9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="328b9-117">-Name</span></span>
<span data-ttu-id="328b9-118">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="328b9-118">Name of cache.</span></span>

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

### <span data-ttu-id="328b9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="328b9-119">-PassThru</span></span>
<span data-ttu-id="328b9-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="328b9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="328b9-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="328b9-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="328b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="328b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="328b9-123">Nome do grupo de recursos no qual você deseja remover o cache.</span><span class="sxs-lookup"><span data-stu-id="328b9-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="328b9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="328b9-124">-Confirm</span></span>
<span data-ttu-id="328b9-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="328b9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="328b9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="328b9-126">-WhatIf</span></span>
<span data-ttu-id="328b9-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="328b9-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="328b9-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="328b9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="328b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="328b9-129">CommonParameters</span></span>
<span data-ttu-id="328b9-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="328b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="328b9-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="328b9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="328b9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="328b9-132">INPUTS</span></span>

### <span data-ttu-id="328b9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="328b9-133">System.String</span></span>

## <span data-ttu-id="328b9-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="328b9-134">OUTPUTS</span></span>

## <span data-ttu-id="328b9-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="328b9-135">NOTES</span></span>

## <span data-ttu-id="328b9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="328b9-136">RELATED LINKS</span></span>
