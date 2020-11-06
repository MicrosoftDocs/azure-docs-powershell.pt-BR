---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 5b1901ef5d06d24e6561861dca3c8e1d89185d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429994"
---
# New-AzureRmSqlElasticPool

## Sinopse
Cria um pool de banco de dados elástico para um banco de dados SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### DtuBasedPool (padrão)
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VcoreBasedPool
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmSqlElasticPool** cria um pool de banco de dados elástico para um banco de dados SQL do Azure.
Vários parâmetros ( *-DTU,-DatabaseDtuMin e-DatabaseDtuMax* ) exigem que o valor definido seja da lista de valores válidos para esse parâmetro. Por exemplo,-DatabaseDtuMax para um pool de eDTU de 100 padrão só pode ser definido como 10, 20, 50 ou 100.  Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).

## EXEMPLOS

### Exemplo 1: criar um pool elástico
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

Esse comando cria um pool elástico na camada de serviço padrão chamada ElasticPool01. O servidor chamado Server01, atribuído a um grupo de recursos do Azure chamado ResourceGroup01, hospeda o pool elástico no. O comando especifica os valores da propriedade DTU para o pool e os bancos de dados no pool.

## OS

### -AsJob
Executar o cmdlet em segundo plano

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

### -ComputeGeneration
A geração de computação a ser atribuída.

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMax
Especifica o número máximo de unidades de produtividade do banco de dados (DTUs) que qualquer único banco de dados no pool pode consumir.
Os valores padrão para as diferentes edições são os seguintes:
- Basic. 5 DTUs
- Oficial. 100 DTUs
- Gratifica. 125 DTUs para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMin
Especifica o número mínimo de DTUs que o pool elástico garante para todos os bancos de dados do pool.
O valor padrão é zero (0).
Para obter detalhes sobre quais valores são válidos, consulte a tabela do seu pool de tamanhos específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMax
O número VCore da Maxmium qualquer banco de dados sqlazure pode consumir no pool.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMin
O número mínimo de VCore que qualquer banco de dados sqlazure pode consumir no pool.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -DTU
Especifica o número total de DTUs compartilhadas para o pool elástico.
Os valores padrão para as diferentes edições são os seguintes:
- Basic.
100 DTUs
- Oficial.
100 DTUs
- Gratifica.
125 DTUs para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticos](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edição
Especifica a edição do banco de dados SQL do Azure usado para o pool elástico.
Os valores aceitáveis para esse parâmetro são:
- Nenhuma
- Basic
- Oficial
- Gratifica
- DataWarehouse
- Gratuito
- Automático
- GeneralPurpose
- BusinessCritical

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolName
Especifica o nome do pool elástico que este cmdlet cria.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
O tipo de licença para o banco de dados SQL do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o pool elástico.

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

### -Nomedoservidor
Especifica o nome do servidor que hospeda o pool elástico.

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

### -StorageMB
Especifica o limite de armazenamento, em megabytes, para o pool elástico. Se você não especificar esse parâmetro, esse cmdlet calculará um valor que depende do valor do parâmetro *DTU* .
Veja [os limites de eDTU e armazenamento](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) para os valores possíveis.

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

### -Marcas
Especifica um dicionário de pares de chave-valor na forma de uma tabela de hash que este cmdlet associa ao pool elástico. Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

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

### -VCore
O número total compartilhado de Vcores para o pool elástico do SQL Azure.

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneRedundant
A redundância de zona para associar ao pool elástico do SQL do Azure

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

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

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Sql. ElasticPool. Model. AzureSqlElasticPoolModel

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSqlElasticPool](./Get-AzureRmSqlElasticPool.md)

[Get-AzureRmSqlElasticPoolActivity](./Get-AzureRmSqlElasticPoolActivity.md)

[Get-AzureRmSqlElasticPoolDatabase](./Get-AzureRmSqlElasticPoolDatabase.md)

[Remove-AzureRmSqlElasticPool](./Remove-AzureRmSqlElasticPool.md)

[Set-AzureRmSqlElasticPool](./Set-AzureRmSqlElasticPool.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)
