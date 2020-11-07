---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF41DDBA-6D4B-47A5-BCFF-3D0BB1D375C5
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2b6aaf5e8564b3eea675a57176b8f7118d2c7a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945960"
---
# Set-AzureHDInsightDefaultStorage

## Sinopse
Define a conta de armazenamento padrão para um cluster HDInsight.

## SYNTAX

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Esta versão do Azure PowerShell HDInsight foi preterida.
Estes cmdlets serão removidos até 1º de janeiro de 2017.
Use a versão mais recente do Azure PowerShell HDInsight.

Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

O cmdlet **set-AzureHDInsightDefaultStorage** define a conta de armazenamento padrão para uma configuração de cluster HDInsight.

## EXEMPLOS

### Exemplo 1: definir a conta de armazenamento padrão
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

O primeiro comando usa o cmdlet **Get-AzureSubscription** para obter a ID de assinatura atual e, em seguida, armazena-a na variável $SubId.

O segundo e terceiro comandos usam o cmdlet **Get-AzureStorageKey** para obter as chaves de armazenamento principal para MyBlobStorage e MySecondBlobStorage e, em seguida, armazenar as chaves nas variáveis $Key 1 e $Key 2, respectivamente.

Os comandos quarto, quinto e sexto usam o cmdlet **Get-Credential** para obter credenciais para a assinatura atual e, em seguida, armazenam as credenciais nas variáveis $Creds, $OozieCreds e $HiveCreds.

O comando final executa uma sequência de operações usando estes cmdlets: 

- **New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight.
- **Set-AzureHDInsightDefaultStorage** para definir a conta de armazenamento padrão para a configuração para MyBlobStorage.blob.Core.Windows.net.
- **Add-AzureHDInsightStorage** para adicionar uma segunda conta de armazenamento chamada MySecondBlobStorage.blob.Core.Windows.net à configuração.
- **Add-AzureHDInsightMetastore** para adicionar um metastore para Oozie e um metastore para Hive à configuração.
- **New-AzureHDInsightCluster** para criar um cluster HDInsight com a nova configuração.

## OS

### -Config
Especifica um objeto de configuração.
Esse cmdlet define a conta de armazenamento padrão para o objeto que esse parâmetro especifica.

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

### -StorageAccountKey
Especifica a chave da conta de armazenamento que é usada para acessar a conta de armazenamento padrão.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Especifica o nome de uma conta de armazenamento padrão.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerName
Especifica o nome do contêiner de armazenamento padrão para um cluster.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)


