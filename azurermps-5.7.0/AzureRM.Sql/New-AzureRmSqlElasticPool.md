---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431571"
---
# <span data-ttu-id="64c74-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="64c74-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="64c74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64c74-102">SYNOPSIS</span></span>
<span data-ttu-id="64c74-103">Cria um pool de banco de dados elástico para um banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="64c74-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64c74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64c74-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64c74-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64c74-105">DESCRIPTION</span></span>
<span data-ttu-id="64c74-106">O cmdlet **New-AzureRmSqlElasticPool** cria um pool de banco de dados elástico para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="64c74-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="64c74-107">Vários parâmetros ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) exigem que o valor definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="64c74-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="64c74-108">Por exemplo,-DatabaseDtuMax para um pool de eDTU de 100 padrão só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="64c74-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="64c74-109">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="64c74-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="64c74-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64c74-110">EXAMPLES</span></span>

### <span data-ttu-id="64c74-111">Exemplo 1: criar um pool elástico</span><span class="sxs-lookup"><span data-stu-id="64c74-111">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="64c74-112">Esse comando cria um pool elástico na camada de serviço padrão chamada ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="64c74-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="64c74-113">O servidor chamado Server01, atribuído a um grupo de recursos do Azure chamado ResourceGroup01, hospeda o pool elástico no.</span><span class="sxs-lookup"><span data-stu-id="64c74-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="64c74-114">O comando especifica os valores da propriedade DTU para o pool e os bancos de dados no pool.</span><span class="sxs-lookup"><span data-stu-id="64c74-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="64c74-115">OS</span><span class="sxs-lookup"><span data-stu-id="64c74-115">PARAMETERS</span></span>

### <span data-ttu-id="64c74-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64c74-116">-AsJob</span></span>
<span data-ttu-id="64c74-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="64c74-117">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="64c74-118">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="64c74-118">-DatabaseDtuMax</span></span>
<span data-ttu-id="64c74-119">Especifica o número máximo de unidades de produtividade do banco de dados (DTUs) que qualquer único banco de dados no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="64c74-119">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="64c74-120">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="64c74-120">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="64c74-121">Basic.</span><span class="sxs-lookup"><span data-stu-id="64c74-121">Basic.</span></span> <span data-ttu-id="64c74-122">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="64c74-122">5 DTUs</span></span>
- <span data-ttu-id="64c74-123">Oficial.</span><span class="sxs-lookup"><span data-stu-id="64c74-123">Standard.</span></span> <span data-ttu-id="64c74-124">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="64c74-124">100 DTUs</span></span>
- <span data-ttu-id="64c74-125">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="64c74-125">Premium.</span></span> <span data-ttu-id="64c74-126">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="64c74-126">125 DTUs</span></span>

<span data-ttu-id="64c74-127">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="64c74-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="64c74-128">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="64c74-128">-DatabaseDtuMin</span></span>
<span data-ttu-id="64c74-129">Especifica o número mínimo de DTUs que o pool elástico garante para todos os bancos de dados do pool.</span><span class="sxs-lookup"><span data-stu-id="64c74-129">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="64c74-130">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="64c74-130">The default value is zero (0).</span></span>

<span data-ttu-id="64c74-131">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="64c74-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="64c74-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c74-132">-DefaultProfile</span></span>
<span data-ttu-id="64c74-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="64c74-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64c74-134">-DTU</span><span class="sxs-lookup"><span data-stu-id="64c74-134">-Dtu</span></span>
<span data-ttu-id="64c74-135">Especifica o número total de DTUs compartilhadas para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="64c74-135">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="64c74-136">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="64c74-136">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="64c74-137">Basic.</span><span class="sxs-lookup"><span data-stu-id="64c74-137">Basic.</span></span>
<span data-ttu-id="64c74-138">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="64c74-138">100 DTUs</span></span>
- <span data-ttu-id="64c74-139">Oficial.</span><span class="sxs-lookup"><span data-stu-id="64c74-139">Standard.</span></span>
<span data-ttu-id="64c74-140">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="64c74-140">100 DTUs</span></span>
- <span data-ttu-id="64c74-141">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="64c74-141">Premium.</span></span>
<span data-ttu-id="64c74-142">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="64c74-142">125 DTUs</span></span>

<span data-ttu-id="64c74-143">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="64c74-143">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="64c74-144">-Edição</span><span class="sxs-lookup"><span data-stu-id="64c74-144">-Edition</span></span>
<span data-ttu-id="64c74-145">Especifica a edição do banco de dados SQL do Azure usado para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="64c74-145">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="64c74-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="64c74-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64c74-147">Gratifica</span><span class="sxs-lookup"><span data-stu-id="64c74-147">Premium</span></span>
- <span data-ttu-id="64c74-148">Basic</span><span class="sxs-lookup"><span data-stu-id="64c74-148">Basic</span></span>
- <span data-ttu-id="64c74-149">Oficial</span><span class="sxs-lookup"><span data-stu-id="64c74-149">Standard</span></span>
- <span data-ttu-id="64c74-150">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="64c74-150">DataWarehouse</span></span>
- <span data-ttu-id="64c74-151">Automático</span><span class="sxs-lookup"><span data-stu-id="64c74-151">Stretch</span></span>

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

### <span data-ttu-id="64c74-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="64c74-152">-ElasticPoolName</span></span>
<span data-ttu-id="64c74-153">Especifica o nome do pool elástico que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="64c74-153">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c74-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c74-154">-ResourceGroupName</span></span>
<span data-ttu-id="64c74-155">Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="64c74-155">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="64c74-156">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="64c74-156">-ServerName</span></span>
<span data-ttu-id="64c74-157">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="64c74-157">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="64c74-158">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="64c74-158">-StorageMB</span></span>
<span data-ttu-id="64c74-159">Especifica o limite de armazenamento, em megabytes, para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="64c74-159">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="64c74-160">Se você não especificar esse parâmetro, esse cmdlet calculará um valor que depende do valor do parâmetro *DTU* .</span><span class="sxs-lookup"><span data-stu-id="64c74-160">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="64c74-161">Veja [os limites de eDTU e armazenamento](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) para os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="64c74-161">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="64c74-162">-Marcas</span><span class="sxs-lookup"><span data-stu-id="64c74-162">-Tags</span></span>
<span data-ttu-id="64c74-163">Especifica um dicionário de pares de chave-valor na forma de uma tabela de hash que este cmdlet associa ao pool elástico.</span><span class="sxs-lookup"><span data-stu-id="64c74-163">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="64c74-164">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="64c74-164">For example:</span></span>

<span data-ttu-id="64c74-165">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="64c74-165">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="64c74-166">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="64c74-166">-ZoneRedundant</span></span>
<span data-ttu-id="64c74-167">A redundância de zona para associar ao pool elástico do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="64c74-167">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="64c74-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64c74-168">-Confirm</span></span>
<span data-ttu-id="64c74-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64c74-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64c74-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64c74-170">-WhatIf</span></span>
<span data-ttu-id="64c74-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64c74-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64c74-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64c74-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64c74-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c74-173">CommonParameters</span></span>
<span data-ttu-id="64c74-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c74-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c74-175">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c74-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c74-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64c74-176">INPUTS</span></span>

### <span data-ttu-id="64c74-177">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="64c74-177">None</span></span>
<span data-ttu-id="64c74-178">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="64c74-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64c74-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64c74-179">OUTPUTS</span></span>

### <span data-ttu-id="64c74-180">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="64c74-180">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="64c74-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64c74-181">NOTES</span></span>

## <span data-ttu-id="64c74-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64c74-182">RELATED LINKS</span></span>

[<span data-ttu-id="64c74-183">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="64c74-183">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="64c74-184">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="64c74-184">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="64c74-185">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="64c74-185">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="64c74-186">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="64c74-186">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="64c74-187">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="64c74-187">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="64c74-188">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="64c74-188">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
