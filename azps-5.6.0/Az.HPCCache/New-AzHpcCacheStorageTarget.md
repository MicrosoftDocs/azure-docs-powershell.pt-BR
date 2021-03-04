---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: deb359905086d68edb4129e023ce6dd8d2ceaf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893343"
---
# <span data-ttu-id="e4055-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="e4055-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="e4055-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4055-102">SYNOPSIS</span></span>
<span data-ttu-id="e4055-103">Cria um Destino de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e4055-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="e4055-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e4055-104">SYNTAX</span></span>

### <span data-ttu-id="e4055-105">ClfsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e4055-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4055-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4055-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4055-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e4055-107">DESCRIPTION</span></span>
<span data-ttu-id="e4055-108">O cmdlet **New-AzHpcCacheStorageTarget** adiciona um Destino de Armazenamento ao Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4055-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="e4055-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4055-109">EXAMPLES</span></span>

### <span data-ttu-id="e4055-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4055-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="e4055-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4055-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="e4055-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e4055-112">PARAMETERS</span></span>

### <span data-ttu-id="e4055-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4055-113">-AsJob</span></span>
<span data-ttu-id="e4055-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e4055-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4055-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="e4055-115">-CacheName</span></span>
<span data-ttu-id="e4055-116">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="e4055-116">Name of cache.</span></span>

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

### <span data-ttu-id="e4055-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="e4055-117">-CLFS</span></span>
<span data-ttu-id="e4055-118">Atualizar o tipo de Destino de Armazenamento CLFS.</span><span class="sxs-lookup"><span data-stu-id="e4055-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="e4055-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4055-119">-DefaultProfile</span></span>
<span data-ttu-id="e4055-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4055-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4055-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e4055-121">-Force</span></span>
<span data-ttu-id="e4055-122">Indica que o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="e4055-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e4055-123">Por padrão, este cmdlet solicita que você confirme se deseja liberar o cache.</span><span class="sxs-lookup"><span data-stu-id="e4055-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="e4055-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="e4055-124">-HostName</span></span>
<span data-ttu-id="e4055-125">Nome do host NFS.</span><span class="sxs-lookup"><span data-stu-id="e4055-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4055-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="e4055-126">-Junction</span></span>
<span data-ttu-id="e4055-127">Junção.</span><span class="sxs-lookup"><span data-stu-id="e4055-127">Junction.</span></span>

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

### <span data-ttu-id="e4055-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e4055-128">-Name</span></span>
<span data-ttu-id="e4055-129">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e4055-129">Name of storage target.</span></span>

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

### <span data-ttu-id="e4055-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="e4055-130">-NFS</span></span>
<span data-ttu-id="e4055-131">Atualizar tipo de destino de armazenamento NFS.</span><span class="sxs-lookup"><span data-stu-id="e4055-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="e4055-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4055-132">-ResourceGroupName</span></span>
<span data-ttu-id="e4055-133">"Nome do grupo de recursos no qual você deseja criar destino de armazenamento para determinado cache.</span><span class="sxs-lookup"><span data-stu-id="e4055-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="e4055-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="e4055-134">-StorageContainerID</span></span>
<span data-ttu-id="e4055-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="e4055-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4055-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="e4055-136">-UsageModel</span></span>
<span data-ttu-id="e4055-137">Modelo de uso do NFS.</span><span class="sxs-lookup"><span data-stu-id="e4055-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4055-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4055-138">-Confirm</span></span>
<span data-ttu-id="e4055-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4055-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4055-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4055-140">-WhatIf</span></span>
<span data-ttu-id="e4055-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4055-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4055-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4055-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4055-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4055-143">CommonParameters</span></span>
<span data-ttu-id="e4055-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4055-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4055-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4055-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4055-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4055-146">INPUTS</span></span>

### <span data-ttu-id="e4055-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e4055-147">System.String</span></span>

## <span data-ttu-id="e4055-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e4055-148">OUTPUTS</span></span>

### <span data-ttu-id="e4055-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="e4055-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="e4055-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="e4055-150">NOTES</span></span>

## <span data-ttu-id="e4055-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4055-151">RELATED LINKS</span></span>
