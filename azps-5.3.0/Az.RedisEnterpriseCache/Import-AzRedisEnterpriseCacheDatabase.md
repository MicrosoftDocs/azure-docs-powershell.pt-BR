---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 6ab4babd894a3c639db6e41e6088653604072c7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271611"
---
# <span data-ttu-id="dac35-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="dac35-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="dac35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dac35-102">SYNOPSIS</span></span>
<span data-ttu-id="dac35-103">Importa um arquivo de banco de dados para o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="dac35-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="dac35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dac35-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dac35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dac35-105">DESCRIPTION</span></span>
<span data-ttu-id="dac35-106">Importa um arquivo de banco de dados para o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="dac35-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="dac35-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dac35-107">EXAMPLES</span></span>

### <span data-ttu-id="dac35-108">Exemplo 1: importar banco de dados</span><span class="sxs-lookup"><span data-stu-id="dac35-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="dac35-109">Esse comando importa um arquivo de banco de dados para o banco de dados do cache corporativo Redis nomeado como myCache.</span><span class="sxs-lookup"><span data-stu-id="dac35-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="dac35-110">Exemplo 2: importar banco de dados (usando o arquivo de exemplo)</span><span class="sxs-lookup"><span data-stu-id="dac35-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="dac35-111">Esse comando importa um arquivo de banco de dados para o banco de dados do cache corporativo Redis nomeado como myCache.</span><span class="sxs-lookup"><span data-stu-id="dac35-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="dac35-112">OS</span><span class="sxs-lookup"><span data-stu-id="dac35-112">PARAMETERS</span></span>

### <span data-ttu-id="dac35-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dac35-113">-AsJob</span></span>
<span data-ttu-id="dac35-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="dac35-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dac35-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dac35-115">-ClusterName</span></span>
<span data-ttu-id="dac35-116">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="dac35-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="dac35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac35-117">-DefaultProfile</span></span>
<span data-ttu-id="dac35-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dac35-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dac35-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="dac35-119">-NoWait</span></span>
<span data-ttu-id="dac35-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="dac35-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dac35-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dac35-121">-PassThru</span></span>
<span data-ttu-id="dac35-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="dac35-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dac35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac35-123">-ResourceGroupName</span></span>
<span data-ttu-id="dac35-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dac35-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="dac35-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="dac35-125">-SasUri</span></span>
<span data-ttu-id="dac35-126">URI da SAS para o qual o blob de destino será importado</span><span class="sxs-lookup"><span data-stu-id="dac35-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="dac35-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dac35-127">-SubscriptionId</span></span>
<span data-ttu-id="dac35-128">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dac35-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dac35-129">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="dac35-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dac35-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dac35-130">-Confirm</span></span>
<span data-ttu-id="dac35-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dac35-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dac35-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dac35-132">-WhatIf</span></span>
<span data-ttu-id="dac35-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dac35-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dac35-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dac35-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dac35-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac35-135">CommonParameters</span></span>
<span data-ttu-id="dac35-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dac35-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac35-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dac35-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac35-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dac35-138">INPUTS</span></span>

## <span data-ttu-id="dac35-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dac35-139">OUTPUTS</span></span>

### <span data-ttu-id="dac35-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dac35-140">System.Boolean</span></span>

## <span data-ttu-id="dac35-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dac35-141">NOTES</span></span>

<span data-ttu-id="dac35-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dac35-142">ALIASES</span></span>

## <span data-ttu-id="dac35-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dac35-143">RELATED LINKS</span></span>

