---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947734"
---
# <span data-ttu-id="e22aa-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="e22aa-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="e22aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e22aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e22aa-103">Cria um destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e22aa-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="e22aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e22aa-104">SYNTAX</span></span>

### <span data-ttu-id="e22aa-105">ClfsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e22aa-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e22aa-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e22aa-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e22aa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e22aa-107">DESCRIPTION</span></span>
<span data-ttu-id="e22aa-108">O cmdlet **New-AzHpcCacheStorageTarget** adiciona um destino de armazenamento ao cache do Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="e22aa-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="e22aa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e22aa-109">EXAMPLES</span></span>

### <span data-ttu-id="e22aa-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e22aa-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="e22aa-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e22aa-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="e22aa-112">OS</span><span class="sxs-lookup"><span data-stu-id="e22aa-112">PARAMETERS</span></span>

### <span data-ttu-id="e22aa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e22aa-113">-AsJob</span></span>
<span data-ttu-id="e22aa-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e22aa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e22aa-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="e22aa-115">-CacheName</span></span>
<span data-ttu-id="e22aa-116">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="e22aa-116">Name of cache.</span></span>

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

### <span data-ttu-id="e22aa-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="e22aa-117">-CLFS</span></span>
<span data-ttu-id="e22aa-118">Atualize o tipo de destino de armazenamento CLFS.</span><span class="sxs-lookup"><span data-stu-id="e22aa-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="e22aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22aa-119">-DefaultProfile</span></span>
<span data-ttu-id="e22aa-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e22aa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e22aa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e22aa-121">-Force</span></span>
<span data-ttu-id="e22aa-122">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="e22aa-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e22aa-123">Por padrão, esse cmdlet solicita que você confirme que deseja liberar o cache.</span><span class="sxs-lookup"><span data-stu-id="e22aa-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="e22aa-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="e22aa-124">-HostName</span></span>
<span data-ttu-id="e22aa-125">Nome do host NFS.</span><span class="sxs-lookup"><span data-stu-id="e22aa-125">NFS host name.</span></span>

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

### <span data-ttu-id="e22aa-126">-Junção</span><span class="sxs-lookup"><span data-stu-id="e22aa-126">-Junction</span></span>
<span data-ttu-id="e22aa-127">Junction.</span><span class="sxs-lookup"><span data-stu-id="e22aa-127">Junction.</span></span>

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

### <span data-ttu-id="e22aa-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e22aa-128">-Name</span></span>
<span data-ttu-id="e22aa-129">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e22aa-129">Name of storage target.</span></span>

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

### <span data-ttu-id="e22aa-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="e22aa-130">-NFS</span></span>
<span data-ttu-id="e22aa-131">Atualize o tipo de destino do armazenamento NFS.</span><span class="sxs-lookup"><span data-stu-id="e22aa-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="e22aa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e22aa-132">-ResourceGroupName</span></span>
<span data-ttu-id="e22aa-133">"Nome do grupo de recursos sob o qual você deseja criar o destino de armazenamento para um determinado cache.</span><span class="sxs-lookup"><span data-stu-id="e22aa-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="e22aa-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="e22aa-134">-StorageContainerID</span></span>
<span data-ttu-id="e22aa-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="e22aa-135">StorageContainerID</span></span>

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

### <span data-ttu-id="e22aa-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="e22aa-136">-UsageModel</span></span>
<span data-ttu-id="e22aa-137">Modelo de uso do NFS.</span><span class="sxs-lookup"><span data-stu-id="e22aa-137">NFS usage model.</span></span>

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

### <span data-ttu-id="e22aa-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e22aa-138">-Confirm</span></span>
<span data-ttu-id="e22aa-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e22aa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e22aa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e22aa-140">-WhatIf</span></span>
<span data-ttu-id="e22aa-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e22aa-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e22aa-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e22aa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e22aa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22aa-143">CommonParameters</span></span>
<span data-ttu-id="e22aa-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e22aa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22aa-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e22aa-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22aa-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e22aa-146">INPUTS</span></span>

### <span data-ttu-id="e22aa-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e22aa-147">System.String</span></span>

## <span data-ttu-id="e22aa-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e22aa-148">OUTPUTS</span></span>

### <span data-ttu-id="e22aa-149">Microsoft. Azure. PowerShell. cmdlets. HPCCache. Models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="e22aa-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="e22aa-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e22aa-150">NOTES</span></span>

## <span data-ttu-id="e22aa-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e22aa-151">RELATED LINKS</span></span>
