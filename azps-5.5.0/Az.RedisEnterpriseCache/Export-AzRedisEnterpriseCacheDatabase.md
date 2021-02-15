---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112663"
---
# <span data-ttu-id="a95eb-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="a95eb-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="a95eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a95eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a95eb-103">Exporta um arquivo de banco de dados do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="a95eb-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="a95eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a95eb-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a95eb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a95eb-105">DESCRIPTION</span></span>
<span data-ttu-id="a95eb-106">Exporta um arquivo de banco de dados do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="a95eb-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="a95eb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a95eb-107">EXAMPLES</span></span>

### <span data-ttu-id="a95eb-108">Exemplo 1: Exportar banco de dados</span><span class="sxs-lookup"><span data-stu-id="a95eb-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="a95eb-109">Esse comando exporta o banco de dados do Cache Corporativo Redis chamado MyCache para um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a95eb-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="a95eb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a95eb-110">PARAMETERS</span></span>

### <span data-ttu-id="a95eb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a95eb-111">-AsJob</span></span>
<span data-ttu-id="a95eb-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a95eb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a95eb-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a95eb-113">-ClusterName</span></span>
<span data-ttu-id="a95eb-114">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="a95eb-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="a95eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95eb-115">-DefaultProfile</span></span>
<span data-ttu-id="a95eb-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a95eb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95eb-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a95eb-117">-NoWait</span></span>
<span data-ttu-id="a95eb-118">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="a95eb-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a95eb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a95eb-119">-PassThru</span></span>
<span data-ttu-id="a95eb-120">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a95eb-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a95eb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95eb-121">-ResourceGroupName</span></span>
<span data-ttu-id="a95eb-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a95eb-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a95eb-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="a95eb-123">-SasUri</span></span>
<span data-ttu-id="a95eb-124">Uri do SAS para o diretório de destino a ser exportado para</span><span class="sxs-lookup"><span data-stu-id="a95eb-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="a95eb-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a95eb-125">-SubscriptionId</span></span>
<span data-ttu-id="a95eb-126">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a95eb-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a95eb-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a95eb-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a95eb-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a95eb-128">-Confirm</span></span>
<span data-ttu-id="a95eb-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a95eb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a95eb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a95eb-130">-WhatIf</span></span>
<span data-ttu-id="a95eb-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a95eb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a95eb-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a95eb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a95eb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95eb-133">CommonParameters</span></span>
<span data-ttu-id="a95eb-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a95eb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95eb-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a95eb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95eb-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="a95eb-136">INPUTS</span></span>

## <span data-ttu-id="a95eb-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="a95eb-137">OUTPUTS</span></span>

### <span data-ttu-id="a95eb-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a95eb-138">System.Boolean</span></span>

## <span data-ttu-id="a95eb-139">Notas</span><span class="sxs-lookup"><span data-stu-id="a95eb-139">NOTES</span></span>

<span data-ttu-id="a95eb-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="a95eb-140">ALIASES</span></span>

## <span data-ttu-id="a95eb-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a95eb-141">RELATED LINKS</span></span>

