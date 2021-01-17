---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426842"
---
# <span data-ttu-id="d083e-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="d083e-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="d083e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d083e-102">SYNOPSIS</span></span>
<span data-ttu-id="d083e-103">Remove um cache HPC.</span><span class="sxs-lookup"><span data-stu-id="d083e-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="d083e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d083e-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d083e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d083e-105">DESCRIPTION</span></span>
<span data-ttu-id="d083e-106">O cmdlet **Remove-AzHpcCache** remove um cache do Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="d083e-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="d083e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d083e-107">EXAMPLES</span></span>

### <span data-ttu-id="d083e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d083e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="d083e-109">OS</span><span class="sxs-lookup"><span data-stu-id="d083e-109">PARAMETERS</span></span>

### <span data-ttu-id="d083e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d083e-110">-AsJob</span></span>
<span data-ttu-id="d083e-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d083e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d083e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d083e-112">-DefaultProfile</span></span>
<span data-ttu-id="d083e-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d083e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d083e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d083e-114">-Force</span></span>
<span data-ttu-id="d083e-115">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="d083e-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="d083e-116">Por padrão, esse cmdlet solicita que você confirme que deseja remover o cache.</span><span class="sxs-lookup"><span data-stu-id="d083e-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="d083e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d083e-117">-Name</span></span>
<span data-ttu-id="d083e-118">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="d083e-118">Name of cache.</span></span>

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

### <span data-ttu-id="d083e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d083e-119">-PassThru</span></span>
<span data-ttu-id="d083e-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d083e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d083e-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d083e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d083e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d083e-122">-ResourceGroupName</span></span>
<span data-ttu-id="d083e-123">Nome do grupo de recursos sob o qual você deseja remover o cache.</span><span class="sxs-lookup"><span data-stu-id="d083e-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="d083e-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d083e-124">-Confirm</span></span>
<span data-ttu-id="d083e-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d083e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d083e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d083e-126">-WhatIf</span></span>
<span data-ttu-id="d083e-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d083e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d083e-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d083e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d083e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d083e-129">CommonParameters</span></span>
<span data-ttu-id="d083e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d083e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d083e-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d083e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d083e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d083e-132">INPUTS</span></span>

### <span data-ttu-id="d083e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d083e-133">System.String</span></span>

## <span data-ttu-id="d083e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d083e-134">OUTPUTS</span></span>

## <span data-ttu-id="d083e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d083e-135">NOTES</span></span>

## <span data-ttu-id="d083e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d083e-136">RELATED LINKS</span></span>
