---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: d60997647ed4f6bb1317148daadcbe4c0e00a5c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893338"
---
# <span data-ttu-id="92de1-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="92de1-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="92de1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92de1-102">SYNOPSIS</span></span>
<span data-ttu-id="92de1-103">Atualiza um Destino de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="92de1-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="92de1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="92de1-104">SYNTAX</span></span>

### <span data-ttu-id="92de1-105">ClfsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="92de1-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92de1-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="92de1-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92de1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="92de1-107">DESCRIPTION</span></span>
<span data-ttu-id="92de1-108">O cmdlet **Set-AzHpcCacheStorageTarget** atualiza um Destino de Armazenamento anexado ao cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="92de1-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="92de1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92de1-109">EXAMPLES</span></span>

### <span data-ttu-id="92de1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92de1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="92de1-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="92de1-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="92de1-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="92de1-112">PARAMETERS</span></span>

### <span data-ttu-id="92de1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92de1-113">-AsJob</span></span>
<span data-ttu-id="92de1-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="92de1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92de1-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="92de1-115">-CacheName</span></span>
<span data-ttu-id="92de1-116">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="92de1-116">Name of cache.</span></span>

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

### <span data-ttu-id="92de1-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="92de1-117">-CLFS</span></span>
<span data-ttu-id="92de1-118">Atualizar o tipo de Destino de Armazenamento CLFS.</span><span class="sxs-lookup"><span data-stu-id="92de1-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92de1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92de1-119">-DefaultProfile</span></span>
<span data-ttu-id="92de1-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92de1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92de1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="92de1-121">-Force</span></span>
<span data-ttu-id="92de1-122">Indica que o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="92de1-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="92de1-123">Por padrão, este cmdlet solicita que você confirme se deseja liberar o cache.</span><span class="sxs-lookup"><span data-stu-id="92de1-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="92de1-124">-Junction</span><span class="sxs-lookup"><span data-stu-id="92de1-124">-Junction</span></span>
<span data-ttu-id="92de1-125">Junção.</span><span class="sxs-lookup"><span data-stu-id="92de1-125">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92de1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="92de1-126">-Name</span></span>
<span data-ttu-id="92de1-127">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="92de1-127">Name of storage target.</span></span>

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

### <span data-ttu-id="92de1-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="92de1-128">-NFS</span></span>
<span data-ttu-id="92de1-129">Atualizar tipo de destino de armazenamento NFS.</span><span class="sxs-lookup"><span data-stu-id="92de1-129">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92de1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92de1-130">-ResourceGroupName</span></span>
<span data-ttu-id="92de1-131">Nome do grupo de recursos no qual você deseja atualizar o destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="92de1-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="92de1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92de1-132">-Confirm</span></span>
<span data-ttu-id="92de1-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92de1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92de1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92de1-134">-WhatIf</span></span>
<span data-ttu-id="92de1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92de1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92de1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92de1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92de1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92de1-137">CommonParameters</span></span>
<span data-ttu-id="92de1-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92de1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92de1-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92de1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92de1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92de1-140">INPUTS</span></span>

### <span data-ttu-id="92de1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="92de1-141">System.String</span></span>

## <span data-ttu-id="92de1-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="92de1-142">OUTPUTS</span></span>

### <span data-ttu-id="92de1-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="92de1-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="92de1-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="92de1-144">NOTES</span></span>

## <span data-ttu-id="92de1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92de1-145">RELATED LINKS</span></span>
