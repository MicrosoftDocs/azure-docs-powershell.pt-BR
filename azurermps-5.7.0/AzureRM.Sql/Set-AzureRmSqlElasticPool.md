---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431551"
---
# <span data-ttu-id="51648-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="51648-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="51648-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51648-102">SYNOPSIS</span></span>
<span data-ttu-id="51648-103">Modifica as propriedades de um pool de banco de dados elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="51648-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51648-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51648-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51648-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51648-105">DESCRIPTION</span></span>
<span data-ttu-id="51648-106">O cmdlet **set-AzureRmSqlElasticPool** define propriedades para um pool elástico no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="51648-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="51648-107">Esse cmdlet pode modificar o eDTUs por pool ( *DTU* ), o tamanho máximo de armazenamento por pool ( *StorageMB* ), o máximo eDTUs por banco de dados ( *DatabaseDtuMax* ) e o mínimo de EDTUs por banco de dados ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="51648-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="51648-108">Vários parâmetros ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) exigem que o valor definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="51648-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="51648-109">Por exemplo,-DatabaseDtuMax para um pool de eDTU de 100 padrão só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="51648-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="51648-110">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="51648-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="51648-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51648-111">EXAMPLES</span></span>

### <span data-ttu-id="51648-112">Exemplo 1: modificar as propriedades de um pool elástico</span><span class="sxs-lookup"><span data-stu-id="51648-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="51648-113">Esse comando modifica as propriedades de um pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="51648-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="51648-114">O comando define o número de DTUs para o pool elástico para 1000 e define as DTUs mínima e máxima.</span><span class="sxs-lookup"><span data-stu-id="51648-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="51648-115">Exemplo 2: modificar o tamanho máximo de armazenamento de um pool elástico</span><span class="sxs-lookup"><span data-stu-id="51648-115">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="51648-116">Esse comando modifica as propriedades de um pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="51648-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="51648-117">O comando define o armazenamento máximo para um pool elástico para 2 TB.</span><span class="sxs-lookup"><span data-stu-id="51648-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="51648-118">OS</span><span class="sxs-lookup"><span data-stu-id="51648-118">PARAMETERS</span></span>

### <span data-ttu-id="51648-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51648-119">-AsJob</span></span>
<span data-ttu-id="51648-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="51648-120">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-121">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="51648-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="51648-122">Especifica o número máximo de DTUs que qualquer único banco de dados no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="51648-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="51648-123">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="51648-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="51648-124">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="51648-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="51648-125">Basic.</span><span class="sxs-lookup"><span data-stu-id="51648-125">Basic.</span></span>  <span data-ttu-id="51648-126">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="51648-126">5 DTUs</span></span>
- <span data-ttu-id="51648-127">Oficial.</span><span class="sxs-lookup"><span data-stu-id="51648-127">Standard.</span></span> <span data-ttu-id="51648-128">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="51648-128">100 DTUs</span></span>
- <span data-ttu-id="51648-129">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="51648-129">Premium.</span></span> <span data-ttu-id="51648-130">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="51648-130">125 DTUs</span></span>


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="51648-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="51648-132">Especifica o número mínimo de DTUs que o pool elástico garante para todos os bancos de dados do pool.</span><span class="sxs-lookup"><span data-stu-id="51648-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="51648-133">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="51648-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="51648-134">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="51648-134">The default value is zero (0).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51648-135">-DefaultProfile</span></span>
<span data-ttu-id="51648-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="51648-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-137">-DTU</span><span class="sxs-lookup"><span data-stu-id="51648-137">-Dtu</span></span>
<span data-ttu-id="51648-138">Especifica o número total de DTUs compartilhadas para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="51648-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="51648-139">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="51648-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="51648-140">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="51648-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="51648-141">Basic.</span><span class="sxs-lookup"><span data-stu-id="51648-141">Basic.</span></span> <span data-ttu-id="51648-142">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="51648-142">100 DTUs</span></span>
- <span data-ttu-id="51648-143">Oficial.</span><span class="sxs-lookup"><span data-stu-id="51648-143">Standard.</span></span> <span data-ttu-id="51648-144">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="51648-144">100 DTUs</span></span>
- <span data-ttu-id="51648-145">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="51648-145">Premium.</span></span> <span data-ttu-id="51648-146">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="51648-146">125 DTUs</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-147">-Edição</span><span class="sxs-lookup"><span data-stu-id="51648-147">-Edition</span></span>
<span data-ttu-id="51648-148">Especifica a edição do banco de dados SQL do Azure para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="51648-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="51648-149">Não é possível alterar a edição.</span><span class="sxs-lookup"><span data-stu-id="51648-149">You cannot change the edition.</span></span> <span data-ttu-id="51648-150">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="51648-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51648-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="51648-151">None</span></span>
- <span data-ttu-id="51648-152">Basic</span><span class="sxs-lookup"><span data-stu-id="51648-152">Basic</span></span>
- <span data-ttu-id="51648-153">Oficial</span><span class="sxs-lookup"><span data-stu-id="51648-153">Standard</span></span>
- <span data-ttu-id="51648-154">Gratifica</span><span class="sxs-lookup"><span data-stu-id="51648-154">Premium</span></span>
- <span data-ttu-id="51648-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="51648-155">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-156">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="51648-156">-ElasticPoolName</span></span>
<span data-ttu-id="51648-157">Especifica o nome do pool elástico.</span><span class="sxs-lookup"><span data-stu-id="51648-157">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51648-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51648-158">-ResourceGroupName</span></span>
<span data-ttu-id="51648-159">Especifica o nome do grupo de recursos ao qual o pool elástico está atribuído.</span><span class="sxs-lookup"><span data-stu-id="51648-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51648-160">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="51648-160">-ServerName</span></span>
<span data-ttu-id="51648-161">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="51648-161">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51648-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="51648-162">-StorageMB</span></span>
<span data-ttu-id="51648-163">Especifica o limite de armazenamento, em megabytes, para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="51648-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="51648-164">Para obter mais informações, consulte o cmdlet New-AzureRmSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="51648-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-165">-Marcas</span><span class="sxs-lookup"><span data-stu-id="51648-165">-Tags</span></span>
<span data-ttu-id="51648-166">Especifica um dicionário de pares de chave-valor que esse cmdlet associa ao pool elástico na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="51648-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="51648-167">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="51648-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="51648-168">-ZoneRedundant</span></span>
<span data-ttu-id="51648-169">A redundância de zona para associar ao pool elástico do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="51648-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51648-170">-Confirm</span></span>
<span data-ttu-id="51648-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51648-171">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51648-172">-WhatIf</span></span>
<span data-ttu-id="51648-173">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51648-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51648-174">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51648-174">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51648-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51648-175">CommonParameters</span></span>
<span data-ttu-id="51648-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51648-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51648-177">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51648-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51648-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51648-178">INPUTS</span></span>

### <span data-ttu-id="51648-179">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="51648-179">None</span></span>
<span data-ttu-id="51648-180">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="51648-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51648-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51648-181">OUTPUTS</span></span>

### <span data-ttu-id="51648-182">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="51648-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="51648-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51648-183">NOTES</span></span>

## <span data-ttu-id="51648-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51648-184">RELATED LINKS</span></span>

[<span data-ttu-id="51648-185">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="51648-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="51648-186">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="51648-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="51648-187">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="51648-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="51648-188">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="51648-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="51648-189">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="51648-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
