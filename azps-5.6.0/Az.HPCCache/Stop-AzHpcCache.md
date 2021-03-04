---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 2d3fd9d44a06c8538233b1f130010e905055912e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893330"
---
# <span data-ttu-id="3c529-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="3c529-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="3c529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c529-102">SYNOPSIS</span></span>
<span data-ttu-id="3c529-103">Interrompe o cache HPC.</span><span class="sxs-lookup"><span data-stu-id="3c529-103">Stops HPC cache.</span></span>

## <span data-ttu-id="3c529-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3c529-104">SYNTAX</span></span>

### <span data-ttu-id="3c529-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3c529-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c529-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c529-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c529-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c529-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c529-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3c529-108">DESCRIPTION</span></span>
<span data-ttu-id="3c529-109">O cmdlet **Stop-AzHpcCache** interrompe um Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c529-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="3c529-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c529-110">EXAMPLES</span></span>

### <span data-ttu-id="3c529-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c529-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="3c529-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3c529-112">PARAMETERS</span></span>

### <span data-ttu-id="3c529-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c529-113">-DefaultProfile</span></span>
<span data-ttu-id="3c529-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c529-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c529-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3c529-115">-Force</span></span>
<span data-ttu-id="3c529-116">Indica que o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="3c529-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="3c529-117">Por padrão, este cmdlet solicita que você confirme se deseja interromper o cache.</span><span class="sxs-lookup"><span data-stu-id="3c529-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="3c529-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c529-118">-InputObject</span></span>
<span data-ttu-id="3c529-119">O objeto cache a ser parar.</span><span class="sxs-lookup"><span data-stu-id="3c529-119">The cache object to stop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c529-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3c529-120">-Name</span></span>
<span data-ttu-id="3c529-121">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="3c529-121">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c529-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c529-122">-PassThru</span></span>
<span data-ttu-id="3c529-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3c529-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c529-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3c529-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c529-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c529-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c529-126">Nome do grupo de recursos no qual você deseja interromper o cache.</span><span class="sxs-lookup"><span data-stu-id="3c529-126">Name of resource group under which you want to stop cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c529-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c529-127">-ResourceId</span></span>
<span data-ttu-id="3c529-128">A id de recurso do Cache</span><span class="sxs-lookup"><span data-stu-id="3c529-128">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c529-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c529-129">-Confirm</span></span>
<span data-ttu-id="3c529-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c529-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c529-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c529-131">-WhatIf</span></span>
<span data-ttu-id="3c529-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c529-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c529-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c529-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c529-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c529-134">CommonParameters</span></span>
<span data-ttu-id="3c529-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c529-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c529-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c529-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c529-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c529-137">INPUTS</span></span>

### <span data-ttu-id="3c529-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3c529-138">System.String</span></span>

## <span data-ttu-id="3c529-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3c529-139">OUTPUTS</span></span>

## <span data-ttu-id="3c529-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="3c529-140">NOTES</span></span>

## <span data-ttu-id="3c529-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c529-141">RELATED LINKS</span></span>
