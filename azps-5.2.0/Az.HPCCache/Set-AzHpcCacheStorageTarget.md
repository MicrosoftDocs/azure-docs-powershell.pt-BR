---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260371"
---
# <span data-ttu-id="a19f7-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="a19f7-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="a19f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a19f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a19f7-103">Atualiza um destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a19f7-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="a19f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a19f7-104">SYNTAX</span></span>

### <span data-ttu-id="a19f7-105">ClfsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a19f7-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a19f7-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a19f7-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a19f7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a19f7-107">DESCRIPTION</span></span>
<span data-ttu-id="a19f7-108">O cmdlet **set-AzHpcCacheStorageTarget** atualiza um destino de armazenamento associado ao cache do Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="a19f7-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="a19f7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a19f7-109">EXAMPLES</span></span>

### <span data-ttu-id="a19f7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a19f7-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="a19f7-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a19f7-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="a19f7-112">OS</span><span class="sxs-lookup"><span data-stu-id="a19f7-112">PARAMETERS</span></span>

### <span data-ttu-id="a19f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a19f7-113">-AsJob</span></span>
<span data-ttu-id="a19f7-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a19f7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a19f7-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="a19f7-115">-CacheName</span></span>
<span data-ttu-id="a19f7-116">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="a19f7-116">Name of cache.</span></span>

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

### <span data-ttu-id="a19f7-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="a19f7-117">-CLFS</span></span>
<span data-ttu-id="a19f7-118">Atualize o tipo de destino de armazenamento CLFS.</span><span class="sxs-lookup"><span data-stu-id="a19f7-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="a19f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19f7-119">-DefaultProfile</span></span>
<span data-ttu-id="a19f7-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a19f7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a19f7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a19f7-121">-Force</span></span>
<span data-ttu-id="a19f7-122">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="a19f7-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="a19f7-123">Por padrão, esse cmdlet solicita que você confirme que deseja liberar o cache.</span><span class="sxs-lookup"><span data-stu-id="a19f7-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="a19f7-124">-Junção</span><span class="sxs-lookup"><span data-stu-id="a19f7-124">-Junction</span></span>
<span data-ttu-id="a19f7-125">Junction.</span><span class="sxs-lookup"><span data-stu-id="a19f7-125">Junction.</span></span>

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

### <span data-ttu-id="a19f7-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a19f7-126">-Name</span></span>
<span data-ttu-id="a19f7-127">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a19f7-127">Name of storage target.</span></span>

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

### <span data-ttu-id="a19f7-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="a19f7-128">-NFS</span></span>
<span data-ttu-id="a19f7-129">Atualize o tipo de destino do armazenamento NFS.</span><span class="sxs-lookup"><span data-stu-id="a19f7-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="a19f7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a19f7-130">-ResourceGroupName</span></span>
<span data-ttu-id="a19f7-131">Nome do grupo de recursos sob o qual você deseja atualizar o destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a19f7-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="a19f7-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a19f7-132">-Confirm</span></span>
<span data-ttu-id="a19f7-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a19f7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a19f7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a19f7-134">-WhatIf</span></span>
<span data-ttu-id="a19f7-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a19f7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a19f7-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a19f7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a19f7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19f7-137">CommonParameters</span></span>
<span data-ttu-id="a19f7-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19f7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19f7-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a19f7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19f7-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a19f7-140">INPUTS</span></span>

### <span data-ttu-id="a19f7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a19f7-141">System.String</span></span>

## <span data-ttu-id="a19f7-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a19f7-142">OUTPUTS</span></span>

### <span data-ttu-id="a19f7-143">Microsoft. Azure. PowerShell. cmdlets. HPCCache. Models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="a19f7-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="a19f7-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a19f7-144">NOTES</span></span>

## <span data-ttu-id="a19f7-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a19f7-145">RELATED LINKS</span></span>
