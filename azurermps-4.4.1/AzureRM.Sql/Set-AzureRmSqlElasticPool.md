---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429026"
---
# <span data-ttu-id="fe4a6-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fe4a6-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="fe4a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4a6-103">Modifica as propriedades de um pool de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe4a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe4a6-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe4a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe4a6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe4a6-106">O cmdlet **set-AzureRmSqlElasticPool** modifica as propriedades de um pool de banco de dados elástico em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-106">The **Set-AzureRmSqlElasticPool** cmdlet modifies properties for an elastic database pool in an Azure SQL Database.</span></span> <span data-ttu-id="fe4a6-107">Esse cmdlet pode modificar as DTUs (unidades de throughput de banco de dados) mínimas por banco de dados, além do máximo de DTUs por banco de dados, o número de DTUs do pool e o limite de armazenamento do pool.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-107">This cmdlet can modify the minimum Database Throughput Units (DTUs) per database in addition to the maximum DTUs per database, the number of DTUs for the pool, and the storage limit for the pool.</span></span>

<span data-ttu-id="fe4a6-108">Vários parâmetros ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) exigem que o valor definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="fe4a6-109">Por exemplo,-DatabaseDtuMax para um pool de eDTU de 100 padrão só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="fe4a6-110">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="fe4a6-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="fe4a6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe4a6-111">EXAMPLES</span></span>

### <span data-ttu-id="fe4a6-112">Exemplo 1: modificar as propriedades de um pool elástico</span><span class="sxs-lookup"><span data-stu-id="fe4a6-112">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="fe4a6-113">Esse comando modifica as propriedades de um pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="fe4a6-114">O comando define o número de DTUs para o pool elástico para 1000 e define as DTUs mínima e máxima.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="fe4a6-115">Exemplo 2: modificar o armazenamento máximo de um pool elástico</span><span class="sxs-lookup"><span data-stu-id="fe4a6-115">Example 2: Modify the max storage of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="fe4a6-116">Esse comando modifica as propriedades de um pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="fe4a6-117">O comando define o armazenamento máximo para um pool elástico para 2 TB.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="fe4a6-118">OS</span><span class="sxs-lookup"><span data-stu-id="fe4a6-118">PARAMETERS</span></span>

### <span data-ttu-id="fe4a6-119">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="fe4a6-119">-DatabaseDtuMax</span></span>
<span data-ttu-id="fe4a6-120">Especifica o número máximo de DTUs que qualquer único banco de dados no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-120">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="fe4a6-121">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="fe4a6-121">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="fe4a6-122">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="fe4a6-122">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="fe4a6-123">Basic.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-123">Basic.</span></span>  <span data-ttu-id="fe4a6-124">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="fe4a6-124">5 DTUs</span></span>
- <span data-ttu-id="fe4a6-125">Oficial.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-125">Standard.</span></span> <span data-ttu-id="fe4a6-126">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="fe4a6-126">100 DTUs</span></span>
- <span data-ttu-id="fe4a6-127">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-127">Premium.</span></span> <span data-ttu-id="fe4a6-128">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="fe4a6-128">125 DTUs</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-129">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="fe4a6-129">-DatabaseDtuMin</span></span>
<span data-ttu-id="fe4a6-130">Especifica o número mínimo de DTUs que o pool elástico garante para todos os bancos de dados do pool.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-130">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="fe4a6-131">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="fe4a6-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="fe4a6-132">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="fe4a6-132">The default value is zero (0).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-133">-DTU</span><span class="sxs-lookup"><span data-stu-id="fe4a6-133">-Dtu</span></span>
<span data-ttu-id="fe4a6-134">Especifica o número total de DTUs compartilhadas para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-134">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="fe4a6-135">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="fe4a6-135">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="fe4a6-136">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="fe4a6-136">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="fe4a6-137">Basic.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-137">Basic.</span></span> <span data-ttu-id="fe4a6-138">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="fe4a6-138">100 DTUs</span></span>
- <span data-ttu-id="fe4a6-139">Oficial.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-139">Standard.</span></span> <span data-ttu-id="fe4a6-140">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="fe4a6-140">100 DTUs</span></span>
- <span data-ttu-id="fe4a6-141">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-141">Premium.</span></span> <span data-ttu-id="fe4a6-142">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="fe4a6-142">125 DTUs</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-143">-Edição</span><span class="sxs-lookup"><span data-stu-id="fe4a6-143">-Edition</span></span>
<span data-ttu-id="fe4a6-144">Especifica a edição do banco de dados SQL do Azure para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-144">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="fe4a6-145">Não é possível alterar a edição.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-145">You cannot change the edition.</span></span> <span data-ttu-id="fe4a6-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fe4a6-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe4a6-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fe4a6-147">None</span></span>
- <span data-ttu-id="fe4a6-148">Basic</span><span class="sxs-lookup"><span data-stu-id="fe4a6-148">Basic</span></span>
- <span data-ttu-id="fe4a6-149">Oficial</span><span class="sxs-lookup"><span data-stu-id="fe4a6-149">Standard</span></span>
- <span data-ttu-id="fe4a6-150">Gratifica</span><span class="sxs-lookup"><span data-stu-id="fe4a6-150">Premium</span></span>
- <span data-ttu-id="fe4a6-151">Gratificantes</span><span class="sxs-lookup"><span data-stu-id="fe4a6-151">PremiumRS</span></span>
- <span data-ttu-id="fe4a6-152">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="fe4a6-152">DataWarehouse</span></span>
- <span data-ttu-id="fe4a6-153">Gratuito</span><span class="sxs-lookup"><span data-stu-id="fe4a6-153">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-154">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fe4a6-154">-ElasticPoolName</span></span>
<span data-ttu-id="fe4a6-155">Especifica o nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-155">Specifies the name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe4a6-156">-ResourceGroupName</span></span>
<span data-ttu-id="fe4a6-157">Especifica o nome do grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-157">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-158">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fe4a6-158">-ServerName</span></span>
<span data-ttu-id="fe4a6-159">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-159">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-160">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="fe4a6-160">-StorageMB</span></span>
<span data-ttu-id="fe4a6-161">Especifica o limite de armazenamento, em megabytes, para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-161">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="fe4a6-162">Para obter mais informações, consulte o cmdlet New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-162">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-163">-Marcas</span><span class="sxs-lookup"><span data-stu-id="fe4a6-163">-Tags</span></span>
<span data-ttu-id="fe4a6-164">Especifica um dicionário de pares de chave-valor que esse cmdlet associa ao pool elástico na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-164">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="fe4a6-165">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fe4a6-165">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-166">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe4a6-166">-Confirm</span></span>
<span data-ttu-id="fe4a6-167">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe4a6-168">-WhatIf</span></span>
<span data-ttu-id="fe4a6-169">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe4a6-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-170">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4a6-171">-DefaultProfile</span></span>
<span data-ttu-id="fe4a6-172">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4a6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4a6-173">CommonParameters</span></span>
<span data-ttu-id="fe4a6-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe4a6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4a6-175">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe4a6-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4a6-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe4a6-176">INPUTS</span></span>

## <span data-ttu-id="fe4a6-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe4a6-177">OUTPUTS</span></span>

### <span data-ttu-id="fe4a6-178">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="fe4a6-178">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="fe4a6-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe4a6-179">NOTES</span></span>

## <span data-ttu-id="fe4a6-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe4a6-180">RELATED LINKS</span></span>

[<span data-ttu-id="fe4a6-181">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fe4a6-181">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="fe4a6-182">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="fe4a6-182">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="fe4a6-183">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="fe4a6-183">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="fe4a6-184">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fe4a6-184">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="fe4a6-185">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="fe4a6-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
