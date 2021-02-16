---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117633"
---
# <span data-ttu-id="e4925-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e4925-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="e4925-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4925-102">SYNOPSIS</span></span>
<span data-ttu-id="e4925-103">Atualiza um Cache HPC.</span><span class="sxs-lookup"><span data-stu-id="e4925-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="e4925-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4925-104">SYNTAX</span></span>

### <span data-ttu-id="e4925-105">FlushParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e4925-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4925-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4925-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4925-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4925-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4925-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4925-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4925-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4925-109">DESCRIPTION</span></span>
<span data-ttu-id="e4925-110">O cmdlet **Update-AzHpcCache** atualiza um Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4925-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="e4925-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4925-111">EXAMPLES</span></span>

### <span data-ttu-id="e4925-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4925-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="e4925-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4925-113">PARAMETERS</span></span>

### <span data-ttu-id="e4925-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4925-114">-AsJob</span></span>
<span data-ttu-id="e4925-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e4925-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4925-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4925-116">-DefaultProfile</span></span>
<span data-ttu-id="e4925-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4925-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4925-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="e4925-118">-Flush</span></span>
<span data-ttu-id="e4925-119">Libera o Cache HPC.</span><span class="sxs-lookup"><span data-stu-id="e4925-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4925-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e4925-120">-Force</span></span>
<span data-ttu-id="e4925-121">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="e4925-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e4925-122">Por padrão, esse cmdlet solicita que você confirme que deseja atualizar o cache.</span><span class="sxs-lookup"><span data-stu-id="e4925-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="e4925-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4925-123">-InputObject</span></span>
<span data-ttu-id="e4925-124">O objeto de cache a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e4925-124">The cache object to update.</span></span>

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

### <span data-ttu-id="e4925-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4925-125">-Name</span></span>
<span data-ttu-id="e4925-126">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="e4925-126">Name of cache.</span></span>

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

### <span data-ttu-id="e4925-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4925-127">-PassThru</span></span>
<span data-ttu-id="e4925-128">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e4925-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e4925-129">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="e4925-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4925-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4925-130">-ResourceGroupName</span></span>
<span data-ttu-id="e4925-131">Nome do grupo de recursos no qual você deseja atualizar o cache.</span><span class="sxs-lookup"><span data-stu-id="e4925-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="e4925-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4925-132">-ResourceId</span></span>
<span data-ttu-id="e4925-133">A ID do recurso do Cache</span><span class="sxs-lookup"><span data-stu-id="e4925-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="e4925-134">-Atualizar</span><span class="sxs-lookup"><span data-stu-id="e4925-134">-Upgrade</span></span>
<span data-ttu-id="e4925-135">Atualize HpcCache.</span><span class="sxs-lookup"><span data-stu-id="e4925-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4925-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e4925-136">-Confirm</span></span>
<span data-ttu-id="e4925-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4925-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4925-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4925-138">-WhatIf</span></span>
<span data-ttu-id="e4925-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e4925-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4925-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4925-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4925-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4925-141">CommonParameters</span></span>
<span data-ttu-id="e4925-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4925-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4925-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4925-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4925-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4925-144">INPUTS</span></span>

### <span data-ttu-id="e4925-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e4925-145">System.String</span></span>

## <span data-ttu-id="e4925-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4925-146">OUTPUTS</span></span>

## <span data-ttu-id="e4925-147">Notas</span><span class="sxs-lookup"><span data-stu-id="e4925-147">NOTES</span></span>

## <span data-ttu-id="e4925-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4925-148">RELATED LINKS</span></span>
