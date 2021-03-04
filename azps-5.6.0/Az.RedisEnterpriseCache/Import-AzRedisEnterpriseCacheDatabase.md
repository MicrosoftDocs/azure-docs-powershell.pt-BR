---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: b7258c552d14a9c7cdeafae5c23908321b0705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891749"
---
# <span data-ttu-id="395f6-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="395f6-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="395f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="395f6-102">SYNOPSIS</span></span>
<span data-ttu-id="395f6-103">Importa um arquivo de banco de dados para o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="395f6-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="395f6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="395f6-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="395f6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="395f6-105">DESCRIPTION</span></span>
<span data-ttu-id="395f6-106">Importa um arquivo de banco de dados para o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="395f6-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="395f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="395f6-107">EXAMPLES</span></span>

### <span data-ttu-id="395f6-108">Exemplo 1: Importar banco de dados</span><span class="sxs-lookup"><span data-stu-id="395f6-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="395f6-109">Este comando importa um arquivo de banco de dados para o banco de dados do Cache da Empresa Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="395f6-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="395f6-110">Exemplo 2: Importar banco de dados (usando nome de arquivo de exemplo)</span><span class="sxs-lookup"><span data-stu-id="395f6-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="395f6-111">Este comando importa um arquivo de banco de dados para o banco de dados do Cache da Empresa Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="395f6-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="395f6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="395f6-112">PARAMETERS</span></span>

### <span data-ttu-id="395f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="395f6-113">-AsJob</span></span>
<span data-ttu-id="395f6-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="395f6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="395f6-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="395f6-115">-ClusterName</span></span>
<span data-ttu-id="395f6-116">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="395f6-116">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395f6-117">-DefaultProfile</span></span>
<span data-ttu-id="395f6-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="395f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f6-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="395f6-119">-NoWait</span></span>
<span data-ttu-id="395f6-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="395f6-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="395f6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="395f6-121">-PassThru</span></span>
<span data-ttu-id="395f6-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="395f6-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="395f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="395f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="395f6-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="395f6-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f6-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="395f6-125">-SasUri</span></span>
<span data-ttu-id="395f6-126">SAS Uri para o blob de destino a ser importado</span><span class="sxs-lookup"><span data-stu-id="395f6-126">SAS Uri for the target blob to import from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f6-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="395f6-127">-SubscriptionId</span></span>
<span data-ttu-id="395f6-128">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="395f6-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="395f6-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="395f6-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395f6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="395f6-130">-Confirm</span></span>
<span data-ttu-id="395f6-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="395f6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="395f6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="395f6-132">-WhatIf</span></span>
<span data-ttu-id="395f6-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="395f6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="395f6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="395f6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="395f6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395f6-135">CommonParameters</span></span>
<span data-ttu-id="395f6-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395f6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395f6-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="395f6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395f6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="395f6-138">INPUTS</span></span>

## <span data-ttu-id="395f6-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="395f6-139">OUTPUTS</span></span>

### <span data-ttu-id="395f6-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="395f6-140">System.Boolean</span></span>

## <span data-ttu-id="395f6-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="395f6-141">NOTES</span></span>

<span data-ttu-id="395f6-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="395f6-142">ALIASES</span></span>

## <span data-ttu-id="395f6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="395f6-143">RELATED LINKS</span></span>

