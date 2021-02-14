---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: a420a7edf1d5fb7133087c5ecb9fcf605cbdddf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110906"
---
# Set-AzSqlElasticPool

## Sinopse
Modifica as propriedades de um pool de banco de dados elástica no Banco de Dados SQL do Azure.

## Sintaxe

### DtuBasedPool (Padrão)
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### VcoreBasedPool
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzSqlElasticPool** define propriedades para um pool elástica no banco de dados SQL do Azure. Esse cmdlet pode modificar os eDTUs por pool *(Dtu),* o tamanho máximo de armazenamento por pool *(StorageMB),* o máximo eDTUs por banco de dados (*DatabaseDtuMax)* e os eDTUs mínimos por banco de dados (*DatabaseDtuMin).*
Vários parâmetros (*-Dtu, -DatabaseDtuMin e -DatabaseDtuMax)* exigem que o valor que está sendo definido seja da lista de valores válidos para esse parâmetro. Por exemplo, -DatabaseDtuMax para um pool eDTU Padrão 100 só pode ser definido como 10, 20, 50 ou 100.  Para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticas.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

## Exemplos

### Exemplo 1: Modificar propriedades para um pool elástica
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

Esse comando modifica as propriedades de um pool elástica chamado elasticpool01. O comando define o número de DTUs para o pool elástica como 1000 e define as DTUs mínima e máxima.

### Exemplo 2: modificar o tamanho máximo de armazenamento de um pool elástica
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

Esse comando modifica as propriedades de um pool elástica chamado elasticpool01. O comando define o armazenamento máximo de um pool elástica para 2 TB.

### Exemplo 3

Modifica as propriedades de um pool de banco de dados elástica no Banco de Dados SQL do Azure. (gerado automaticamente)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## Parâmetros

### -AsJob
Executar cmdlet em segundo plano

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
A geração de computação a ser atribuir.

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMax
Especifica o número máximo de DTUs que qualquer banco de dados único no pool pode consumir.
Para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticas.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
Os valores padrão para edições diferentes são os mesmos:
- Basic.  5 DTUs
- Padrão. 100 DTUs
- Premium. 125 DTUs

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
Especifica o número mínimo de DTUs que o pool elástica garante a todos os bancos de dados do pool.
Para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticas.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
O valor padrão é zero (0).

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
O número máximo de VCore que qualquer Banco de Dados do SqlAzure pode consumir no pool.

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
O número mínimo de VCore que qualquer Banco de Dados sqlAzure pode consumir no pool.

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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

### -Dtu
Especifica o número total de DTUs compartilhadas para o pool elástica.
Para obter detalhes sobre quais valores são válidos, consulte a tabela do pool de tamanho específico em [pools elásticas.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
Os valores padrão para edições diferentes são os mesmos:
- Basic. 100 DTUs
- Padrão. 100 DTUs
- Premium. 125 DTUs

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
Especifica a edição do Banco de Dados SQL do Azure para o pool elástica. Não é possível alterar a edição. Os valores aceitáveis para este parâmetro são:
- Nenhum
- Basic
- Padrão
- Premium
- Datawarehouse
- Livre
- Esticar
- GeneralPurpose
- BusinessCritical

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

### -ElasticPoolName
Especifica o nome do pool elástica.

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

### -LicenseType
O tipo de licença do banco de dados Sql do Azure.

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

### -MaintenanceConfigurationId
A ID de configuração de manutenção do Pool Elástica SQL.

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
Especifica o nome do grupo de recursos ao qual o pool elástica é atribuído.

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

### -ServerName
Especifica o nome do servidor que hospeda o pool elástica.

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
Especifica o limite de armazenamento, em megabytes, para o pool elástica. Para obter mais informações, consulte o New-AzSqlElasticPool cmdlet.

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
Especifica um dicionário de pares de valor-chave que este cmdlet associa ao pool elástica na forma de uma tabela hash. Por exemplo: `@{key0="value0";"key 1"=$null;key2="value2"}`

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
O número total compartilhado de Vcore para o Pool Elástica do Sql Azure.

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneRedundant
Redundância de zona a ser associada ao Pool Elástica sql do Azure

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

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel

## Notas

## LINKS RELACIONADOS

[Get-AzSqlElasticPool](./Get-AzSqlElasticPool.md)

[Get-AzSqlElasticPoolActivity](./Get-AzSqlElasticPoolActivity.md)

[Get-AzSqlElasticPoolDatabase](./Get-AzSqlElasticPoolDatabase.md)

[New-AzSqlElasticPool](./New-AzSqlElasticPool.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)
