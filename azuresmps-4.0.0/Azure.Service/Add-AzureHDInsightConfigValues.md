---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945728"
---
# Add-AzureHDInsightConfigValues

## Sinopse
Adiciona uma personalização de valor de configuração Hadoop ou uma personalização de biblioteca compartilhada de Hive a uma configuração de cluster HDInsight.

## SYNTAX

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Esta versão do Azure PowerShell HDInsight foi preterida.
Estes cmdlets serão removidos até 1º de janeiro de 2017.
Use a versão mais recente do Azure PowerShell HDInsight.

Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).
Para obter informações sobre como enviar trabalhos usando o PowerShell do Azure e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).
Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets Hdinsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx).

O cmdlet **Add-AzureHDInsightConfigValues** adiciona uma personalização de valor de configuração Hadoop, como Core-site.xml ou Hive-site.xml ou uma personalização de biblioteca compartilhada de Hive para uma configuração de cluster do Azure HDInsight.

O cmdlet adiciona valores de configuração personalizados a um objeto de configuração especificado.
As configurações personalizadas são adicionadas aos arquivos de configuração dos serviços Hadoop relevantes quando o cluster é implantado.

## EXEMPLOS

### Exemplo 1: configurar um cluster
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

O primeiro comando cria um novo objeto **AzureHDInsightHiveConfiguration** e, em seguida, armazena-o na variável $HiveConfigValues.

Os próximos cinco comandos criam valores de configuração para Hive e armazenam esses valores como membros de $HiveConfigValues.

O sétimo comando cria um objeto **AzureHDInsightOozieConfiguration** e, em seguida, armazena-o na variável $OozieConfigValues.
O oitavo comando cria um valor de configuração para Oozie e, em seguida, armazena esses valores como membro de $OozieConfigValues.

O nono comando cria um objeto **AzureHDInsightMapReduceConfiguration** e, em seguida, armazena-o na variável $MapredConfigValues.
Os próximos dois comandos criam valores de configuração para a MapReduce e armazenam esses valores como membros de $MapredConfigValues.

O décimo segundo comando usa o cmdlet **New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight e, em seguida, armazena-a na variável $config.
O comando usa o operador de pipeline para passar $Config para o cmdlet **set-AzureHDInsightDefaultStorage** para atualizar a configuração de armazenamento padrão e para o cmdlet **Add-AzureHDInsightConfigValues** para adicionar os novos valores de configuração à configuração de cluster.

O comando final usa o operador pipeline para passar $Config para o cmdlet **New-AzureHDInsightCluster** para criar um novo cluster HDInsight com as configurações personalizadas.

## OS

### -Config
Especifica o objeto de configuração ao qual adicionar uma configuração Hadoop.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Core
Especifica um conjunto de valores de configuração Hadoop para Core-site.xml.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HBase
Especifica um conjunto de valores de configuração do HBase para Hbase-site.xml.

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HDFS
Especifica um conjunto de valores de configuração Hadoop para Hdfs-site.xml.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hive
Especifica um objeto de personalização para o serviço de Hive Hadoop, incluindo um conjunto de valores de configuração Hadoop para bibliotecas de Hive-site.xml e Hive compartilhado.

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MapReduce
Especifica um objeto de personalização para a MapReduce e o Agendador de capacidade.

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Oozie
Especifica um objeto de personalização para o serviço Hadoop Oozie, incluindo um conjunto de valores de configuração Hadoop para Oozie-site.xml.

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Spark
Especifica um objeto customizado para o Apache Spark.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Storm
Especifica um objeto de personalização para o Apache Storm.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yarn
Especifica um objeto de personalização para o Hadoop YARN, especificando um conjunto de valores de configuração de YARN personalizados para Yarn-site.xml.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
