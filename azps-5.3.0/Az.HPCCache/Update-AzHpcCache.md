---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429276"
---
# <span data-ttu-id="89556-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="89556-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="89556-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89556-102">SYNOPSIS</span></span>
<span data-ttu-id="89556-103">Atualiza um cache HPC.</span><span class="sxs-lookup"><span data-stu-id="89556-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="89556-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89556-104">SYNTAX</span></span>

### <span data-ttu-id="89556-105">FlushParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="89556-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89556-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89556-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89556-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="89556-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89556-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89556-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89556-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89556-109">DESCRIPTION</span></span>
<span data-ttu-id="89556-110">O cmdlet **Update-AzHpcCache** atualiza um cache do Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="89556-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="89556-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89556-111">EXAMPLES</span></span>

### <span data-ttu-id="89556-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89556-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="89556-113">OS</span><span class="sxs-lookup"><span data-stu-id="89556-113">PARAMETERS</span></span>

### <span data-ttu-id="89556-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89556-114">-AsJob</span></span>
<span data-ttu-id="89556-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="89556-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89556-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89556-116">-DefaultProfile</span></span>
<span data-ttu-id="89556-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89556-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89556-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="89556-118">-Flush</span></span>
<span data-ttu-id="89556-119">Libera o cache do HPC.</span><span class="sxs-lookup"><span data-stu-id="89556-119">Flushes HPC Cache.</span></span>

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

### <span data-ttu-id="89556-120">-Force</span><span class="sxs-lookup"><span data-stu-id="89556-120">-Force</span></span>
<span data-ttu-id="89556-121">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="89556-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="89556-122">Por padrão, esse cmdlet solicita que você confirme que deseja atualizar o cache.</span><span class="sxs-lookup"><span data-stu-id="89556-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="89556-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89556-123">-InputObject</span></span>
<span data-ttu-id="89556-124">O objeto de cache para atualizar.</span><span class="sxs-lookup"><span data-stu-id="89556-124">The cache object to update.</span></span>

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

### <span data-ttu-id="89556-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="89556-125">-Name</span></span>
<span data-ttu-id="89556-126">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="89556-126">Name of cache.</span></span>

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

### <span data-ttu-id="89556-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89556-127">-PassThru</span></span>
<span data-ttu-id="89556-128">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="89556-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89556-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="89556-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="89556-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89556-130">-ResourceGroupName</span></span>
<span data-ttu-id="89556-131">Nome do grupo de recursos sob o qual você deseja atualizar o cache.</span><span class="sxs-lookup"><span data-stu-id="89556-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="89556-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89556-132">-ResourceId</span></span>
<span data-ttu-id="89556-133">A ID do recurso do cache</span><span class="sxs-lookup"><span data-stu-id="89556-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="89556-134">-Atualização</span><span class="sxs-lookup"><span data-stu-id="89556-134">-Upgrade</span></span>
<span data-ttu-id="89556-135">Atualize o HpcCache.</span><span class="sxs-lookup"><span data-stu-id="89556-135">Upgrade HpcCache.</span></span>

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

### <span data-ttu-id="89556-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89556-136">-Confirm</span></span>
<span data-ttu-id="89556-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89556-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89556-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89556-138">-WhatIf</span></span>
<span data-ttu-id="89556-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89556-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89556-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89556-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89556-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89556-141">CommonParameters</span></span>
<span data-ttu-id="89556-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89556-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89556-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89556-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89556-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89556-144">INPUTS</span></span>

### <span data-ttu-id="89556-145">System. String</span><span class="sxs-lookup"><span data-stu-id="89556-145">System.String</span></span>

## <span data-ttu-id="89556-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89556-146">OUTPUTS</span></span>

## <span data-ttu-id="89556-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89556-147">NOTES</span></span>

## <span data-ttu-id="89556-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89556-148">RELATED LINKS</span></span>
