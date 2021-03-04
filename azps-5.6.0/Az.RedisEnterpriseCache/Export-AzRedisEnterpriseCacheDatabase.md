---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 3576cfb8185898ea7bb0fa2052a18b651d1d5cc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891757"
---
# <span data-ttu-id="ca044-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="ca044-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="ca044-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca044-102">SYNOPSIS</span></span>
<span data-ttu-id="ca044-103">Exporta um arquivo de banco de dados do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="ca044-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="ca044-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ca044-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ca044-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ca044-105">DESCRIPTION</span></span>
<span data-ttu-id="ca044-106">Exporta um arquivo de banco de dados do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="ca044-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="ca044-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca044-107">EXAMPLES</span></span>

### <span data-ttu-id="ca044-108">Exemplo 1: Exportar banco de dados</span><span class="sxs-lookup"><span data-stu-id="ca044-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="ca044-109">Este comando exporta o banco de dados do Cache corporativo Redis chamado MyCache para um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ca044-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="ca044-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ca044-110">PARAMETERS</span></span>

### <span data-ttu-id="ca044-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca044-111">-AsJob</span></span>
<span data-ttu-id="ca044-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ca044-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ca044-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ca044-113">-ClusterName</span></span>
<span data-ttu-id="ca044-114">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ca044-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="ca044-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca044-115">-DefaultProfile</span></span>
<span data-ttu-id="ca044-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca044-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca044-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ca044-117">-NoWait</span></span>
<span data-ttu-id="ca044-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ca044-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ca044-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca044-119">-PassThru</span></span>
<span data-ttu-id="ca044-120">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ca044-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ca044-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca044-121">-ResourceGroupName</span></span>
<span data-ttu-id="ca044-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca044-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca044-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="ca044-123">-SasUri</span></span>
<span data-ttu-id="ca044-124">SAS Uri para o diretório de destino a ser exportado para</span><span class="sxs-lookup"><span data-stu-id="ca044-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="ca044-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca044-125">-SubscriptionId</span></span>
<span data-ttu-id="ca044-126">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ca044-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ca044-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ca044-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ca044-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca044-128">-Confirm</span></span>
<span data-ttu-id="ca044-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca044-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca044-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca044-130">-WhatIf</span></span>
<span data-ttu-id="ca044-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca044-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca044-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca044-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca044-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca044-133">CommonParameters</span></span>
<span data-ttu-id="ca044-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca044-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca044-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca044-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca044-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca044-136">INPUTS</span></span>

## <span data-ttu-id="ca044-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ca044-137">OUTPUTS</span></span>

### <span data-ttu-id="ca044-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca044-138">System.Boolean</span></span>

## <span data-ttu-id="ca044-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="ca044-139">NOTES</span></span>

<span data-ttu-id="ca044-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ca044-140">ALIASES</span></span>

## <span data-ttu-id="ca044-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca044-141">RELATED LINKS</span></span>

