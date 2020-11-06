---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611082"
---
# <span data-ttu-id="f95c6-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f95c6-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="f95c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f95c6-102">SYNOPSIS</span></span>
<span data-ttu-id="f95c6-103">Cria um pool de banco de dados elástico para um banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="f95c6-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f95c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f95c6-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f95c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f95c6-105">DESCRIPTION</span></span>
<span data-ttu-id="f95c6-106">O cmdlet **New-AzureRmSqlElasticPool** cria um pool de banco de dados elástico para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f95c6-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="f95c6-107">Vários parâmetros ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) exigem que o valor definido seja da lista de valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f95c6-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="f95c6-108">Por exemplo,-DatabaseDtuMax para um pool de eDTU de 100 padrão só pode ser definido como 10, 20, 50 ou 100.</span><span class="sxs-lookup"><span data-stu-id="f95c6-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="f95c6-109">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f95c6-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="f95c6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f95c6-110">EXAMPLES</span></span>

### <span data-ttu-id="f95c6-111">Exemplo 1: criar um pool elástico</span><span class="sxs-lookup"><span data-stu-id="f95c6-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="f95c6-112">Esse comando cria um pool elástico na camada de serviço padrão chamada ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="f95c6-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="f95c6-113">O servidor chamado Server01, atribuído a um grupo de recursos do Azure chamado ResourceGroup01, hospeda o pool elástico no.</span><span class="sxs-lookup"><span data-stu-id="f95c6-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="f95c6-114">O comando especifica os valores da propriedade DTU para o pool e os bancos de dados no pool.</span><span class="sxs-lookup"><span data-stu-id="f95c6-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="f95c6-115">OS</span><span class="sxs-lookup"><span data-stu-id="f95c6-115">PARAMETERS</span></span>

### <span data-ttu-id="f95c6-116">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="f95c6-116">-DatabaseDtuMax</span></span>
<span data-ttu-id="f95c6-117">Especifica o número máximo de unidades de produtividade do banco de dados (DTUs) que qualquer único banco de dados no pool pode consumir.</span><span class="sxs-lookup"><span data-stu-id="f95c6-117">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="f95c6-118">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f95c6-118">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="f95c6-119">Basic.</span><span class="sxs-lookup"><span data-stu-id="f95c6-119">Basic.</span></span> <span data-ttu-id="f95c6-120">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="f95c6-120">5 DTUs</span></span>
- <span data-ttu-id="f95c6-121">Oficial.</span><span class="sxs-lookup"><span data-stu-id="f95c6-121">Standard.</span></span> <span data-ttu-id="f95c6-122">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="f95c6-122">100 DTUs</span></span>
- <span data-ttu-id="f95c6-123">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="f95c6-123">Premium.</span></span> <span data-ttu-id="f95c6-124">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="f95c6-124">125 DTUs</span></span>

<span data-ttu-id="f95c6-125">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="f95c6-125">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="f95c6-126">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="f95c6-126">-DatabaseDtuMin</span></span>
<span data-ttu-id="f95c6-127">Especifica o número mínimo de DTUs que o pool elástico garante para todos os bancos de dados do pool.</span><span class="sxs-lookup"><span data-stu-id="f95c6-127">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="f95c6-128">O valor padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="f95c6-128">The default value is zero (0).</span></span>

<span data-ttu-id="f95c6-129">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f95c6-129">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="f95c6-130">-DTU</span><span class="sxs-lookup"><span data-stu-id="f95c6-130">-Dtu</span></span>
<span data-ttu-id="f95c6-131">Especifica o número total de DTUs compartilhadas para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f95c6-131">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="f95c6-132">Os valores padrão para as diferentes edições são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f95c6-132">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="f95c6-133">Basic.</span><span class="sxs-lookup"><span data-stu-id="f95c6-133">Basic.</span></span>
<span data-ttu-id="f95c6-134">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="f95c6-134">100 DTUs</span></span>
- <span data-ttu-id="f95c6-135">Oficial.</span><span class="sxs-lookup"><span data-stu-id="f95c6-135">Standard.</span></span>
<span data-ttu-id="f95c6-136">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="f95c6-136">100 DTUs</span></span>
- <span data-ttu-id="f95c6-137">Gratifica.</span><span class="sxs-lookup"><span data-stu-id="f95c6-137">Premium.</span></span>
<span data-ttu-id="f95c6-138">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="f95c6-138">125 DTUs</span></span>

<span data-ttu-id="f95c6-139">Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f95c6-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="f95c6-140">-Edição</span><span class="sxs-lookup"><span data-stu-id="f95c6-140">-Edition</span></span>
<span data-ttu-id="f95c6-141">Especifica a edição do banco de dados SQL do Azure usado para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f95c6-141">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="f95c6-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f95c6-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f95c6-143">Gratifica</span><span class="sxs-lookup"><span data-stu-id="f95c6-143">Premium</span></span>
- <span data-ttu-id="f95c6-144">Basic</span><span class="sxs-lookup"><span data-stu-id="f95c6-144">Basic</span></span>
- <span data-ttu-id="f95c6-145">Oficial</span><span class="sxs-lookup"><span data-stu-id="f95c6-145">Standard</span></span>
- <span data-ttu-id="f95c6-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="f95c6-146">DataWarehouse</span></span>
- <span data-ttu-id="f95c6-147">Automático</span><span class="sxs-lookup"><span data-stu-id="f95c6-147">Stretch</span></span>
- <span data-ttu-id="f95c6-148">Gratuito</span><span class="sxs-lookup"><span data-stu-id="f95c6-148">Free</span></span>
- <span data-ttu-id="f95c6-149">Gratificantes</span><span class="sxs-lookup"><span data-stu-id="f95c6-149">PremiumRS</span></span>

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

### <span data-ttu-id="f95c6-150">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f95c6-150">-ElasticPoolName</span></span>
<span data-ttu-id="f95c6-151">Especifica o nome do pool elástico que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="f95c6-151">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f95c6-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95c6-152">-ResourceGroupName</span></span>
<span data-ttu-id="f95c6-153">Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f95c6-153">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="f95c6-154">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f95c6-154">-ServerName</span></span>
<span data-ttu-id="f95c6-155">Especifica o nome do servidor que hospeda o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f95c6-155">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="f95c6-156">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="f95c6-156">-StorageMB</span></span>
<span data-ttu-id="f95c6-157">Especifica o limite de armazenamento, em megabytes, para o pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f95c6-157">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="f95c6-158">Se você não especificar esse parâmetro, esse cmdlet calculará um valor que depende do valor do parâmetro *DTU* .</span><span class="sxs-lookup"><span data-stu-id="f95c6-158">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="f95c6-159">Veja [os limites de eDTU e armazenamento](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) para os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="f95c6-159">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="f95c6-160">-Marcas</span><span class="sxs-lookup"><span data-stu-id="f95c6-160">-Tags</span></span>
<span data-ttu-id="f95c6-161">Especifica um dicionário de pares de chave-valor na forma de uma tabela de hash que este cmdlet associa ao pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f95c6-161">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="f95c6-162">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f95c6-162">For example:</span></span>

<span data-ttu-id="f95c6-163">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f95c6-163">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f95c6-164">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f95c6-164">-Confirm</span></span>
<span data-ttu-id="f95c6-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f95c6-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95c6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95c6-166">-WhatIf</span></span>
<span data-ttu-id="f95c6-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f95c6-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95c6-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f95c6-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95c6-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95c6-169">-DefaultProfile</span></span>
<span data-ttu-id="f95c6-170">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f95c6-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f95c6-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95c6-171">CommonParameters</span></span>
<span data-ttu-id="f95c6-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95c6-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95c6-173">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f95c6-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95c6-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f95c6-174">INPUTS</span></span>

## <span data-ttu-id="f95c6-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f95c6-175">OUTPUTS</span></span>

### <span data-ttu-id="f95c6-176">Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="f95c6-176">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="f95c6-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f95c6-177">NOTES</span></span>

## <span data-ttu-id="f95c6-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f95c6-178">RELATED LINKS</span></span>

[<span data-ttu-id="f95c6-179">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f95c6-179">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f95c6-180">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f95c6-180">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="f95c6-181">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f95c6-181">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="f95c6-182">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f95c6-182">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f95c6-183">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f95c6-183">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f95c6-184">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f95c6-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
