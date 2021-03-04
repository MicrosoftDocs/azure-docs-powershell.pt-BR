---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 9ad46b21990e6a864408536bf56bb09c2d0b3dc3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893340"
---
# <span data-ttu-id="4d581-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="4d581-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="4d581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d581-102">SYNOPSIS</span></span>
<span data-ttu-id="4d581-103">Atualiza marcas em um Cache HPC.</span><span class="sxs-lookup"><span data-stu-id="4d581-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="4d581-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4d581-104">SYNTAX</span></span>

### <span data-ttu-id="4d581-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4d581-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d581-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d581-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d581-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4d581-107">DESCRIPTION</span></span>
<span data-ttu-id="4d581-108">O cmdlet **Set-AzHpcCache** atualiza uma marca de Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d581-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="4d581-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d581-109">EXAMPLES</span></span>

### <span data-ttu-id="4d581-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d581-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="4d581-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4d581-111">PARAMETERS</span></span>

### <span data-ttu-id="4d581-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d581-112">-AsJob</span></span>
<span data-ttu-id="4d581-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4d581-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d581-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d581-114">-DefaultProfile</span></span>
<span data-ttu-id="4d581-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d581-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d581-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d581-116">-InputObject</span></span>
<span data-ttu-id="4d581-117">O objeto cache a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4d581-117">The cache object to update.</span></span>

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

### <span data-ttu-id="4d581-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4d581-118">-Name</span></span>
<span data-ttu-id="4d581-119">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="4d581-119">Name of cache.</span></span>

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

### <span data-ttu-id="4d581-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d581-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d581-121">Nome do grupo de recursos no qual você deseja atualizar o cache.</span><span class="sxs-lookup"><span data-stu-id="4d581-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="4d581-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d581-122">-Tag</span></span>
<span data-ttu-id="4d581-123">As marcas a associar ao Cache HPC.</span><span class="sxs-lookup"><span data-stu-id="4d581-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d581-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d581-124">-Confirm</span></span>
<span data-ttu-id="4d581-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d581-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d581-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d581-126">-WhatIf</span></span>
<span data-ttu-id="4d581-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d581-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d581-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d581-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d581-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d581-129">CommonParameters</span></span>
<span data-ttu-id="4d581-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d581-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d581-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d581-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d581-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d581-132">INPUTS</span></span>

### <span data-ttu-id="4d581-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4d581-133">System.String</span></span>

### <span data-ttu-id="4d581-134">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4d581-134">System.Int32</span></span>

## <span data-ttu-id="4d581-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4d581-135">OUTPUTS</span></span>

### <span data-ttu-id="4d581-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="4d581-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="4d581-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="4d581-137">NOTES</span></span>

## <span data-ttu-id="4d581-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d581-138">RELATED LINKS</span></span>
