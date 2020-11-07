---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945920"
---
# New-AzureHDInsightClusterConfig

## Sinopse
Cria uma configuração de cluster HDInsight não persistente.

## SYNTAX

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Esta versão do Azure PowerShell HDInsight foi preterida.
Estes cmdlets serão removidos até 1º de janeiro de 2017.
Use a versão mais recente do Azure PowerShell HDInsight.

Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

O cmdlet **New-AzureHDInsightClusterConfig** cria uma configuração de cluster do Azure HDInsight não persistente.

## EXEMPLOS

### Exemplo 1: criar uma configuração de cluster
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

O primeiro comando usa o cmdlet **Get-AzureSubscription** para obter a ID de assinatura atual e, em seguida, armazena-a na variável $SubId.

O segundo e terceiro comandos usam o cmdlet **Get-AzureStorageKey** para obter as chaves de armazenamento principal para MyBlobStorage e MySecondBlobStorage e, em seguida, armazenar as chaves nas variáveis $Key 1 e $Key 2, respectivamente.

Os comandos quarto, quinto e sexto usam o cmdlet **Get-Credential** para obter credenciais para a assinatura atual e para Oozie e Hive e, em seguida, armazenar as credenciais em variáveis.

O comando final executa uma sequência de operações usando estes cmdlets: 

- **New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight.
- **Set-AzureHDInsightDefaultStorage** para definir a conta de armazenamento padrão para a configuração para MyBlobStorage.blob.Core.Windows.net.
- **Add-AzureHDInsightStorage** para adicionar uma segunda conta de armazenamento chamada MySecondBlobStorage.blob.Core.Windows.net à configuração.
- **Add-AzureHDInsightMetastore** para adicionar um metastore para Oozie e um metastore para Hive à configuração.
- **New-AzureHDInsightCluster** para criar um cluster HDInsight com a nova configuração.

## OS

### -ClusterSizeInNodes
Especifica o número de nós de dados a serem criados para um cluster.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Clustertype
Especifica o tipo de cluster a ser criado.

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataNodeVMSize
Especifica o tamanho da máquina virtual para o nó de dados.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HeadNodeVMSize
Especifica o tamanho da máquina virtual do nó principal do cluster.

```yaml
Type: String
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

### -SubnetName
Especifica o nome de uma sub-rede.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkId
Especifica a ID da rede virtual para a qual provisionar o cluster.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZookeeperNodeVMSize
Especifica o tamanho da máquina virtual para o nó administradora de um cluster HBase ou Storm.

```yaml
Type: String
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

[Add-AzureHDInsightMetastore](./Add-AzureHDInsightMetastore.md)

[Add-AzureHDInsightStorage](./Add-AzureHDInsightStorage.md)

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Set-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)


