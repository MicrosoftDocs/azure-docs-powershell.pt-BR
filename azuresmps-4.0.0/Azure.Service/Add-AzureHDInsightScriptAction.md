---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945720"
---
# Add-AzureHDInsightScriptAction

## Sinopse
Adiciona uma ação de script HDInsight.

## SYNTAX

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
Esta versão do Azure PowerShell HDInsight foi preterida.
Estes cmdlets serão removidos até 1º de janeiro de 2017.
Use a versão mais recente do Azure PowerShell HDInsight.

Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

O cmdlet **Add-AzureHDInsightScriptAction** fornece a funcionalidade do Azure HDInsight que é usada para instalar software adicional ou alterar a configuração de aplicativos executados em um cluster Hadoop usando scripts do Windows PowerShell.

Uma ação de script é executada nos nós de cluster quando os clusters HDInsight são implantados e eles são executados após nós no cluster concluir a configuração do HDInsight.
A ação de script é executada em privilégios de conta de administrador do sistema e fornece direitos de acesso completo aos nós de cluster.
Você pode fornecer a cada cluster uma lista de ações de script a serem executadas em uma sequência específica.

## EXEMPLOS

### Exemplo 1: adicionar uma ação de script a um cluster
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

O primeiro comando usa o cmdlet **New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight e, em seguida, armazena-o na variável $config.

O segundo comando usa o cmdlet **Add-AzureHDInsightScriptAction** para adicionar a ação de script chamada TestScriptAction a $config.

O comando final usa o cmdlet **New-AzureHDInsightCluster** para criar um novo cluster HDInsight que executa a ação de script armazenada em $config.

### Exemplo 2: adicionar várias ações de script a um cluster
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

O primeiro comando usa o cmdlet **New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight e, em seguida, armazena-o na variável $config.

O segundo comando usa o cmdlet **Add-AzureHDInsightScriptAction** para adicionar a ação de script especificada a $config e, em seguida, usa o operador pipeline para passar $config para **Add-AzureHDInsightScriptAction** uma segunda vez para adicionar uma segunda ação de script para $config.

O comando final usa o cmdlet **New-AzureHDInsightCluster** para criar um cluster que executa as ações de script no $config.

## OS

### -ClusterRoleCollection
Especifica os nós para os quais executar um script.
Os valores aceitáveis para esse parâmetro são: HeadNode ou datanode.

Você pode especificar um valor ou os dois valores.

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Especifica um objeto de configuração.
Esse cmdlet adiciona informações de ação de script ao objeto que esse parâmetro especifica.

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

### -Nome
Especifica o nome de uma ação de script.

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

### -Parâmetros
Especifica os parâmetros necessários para uma ação de script.

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

### -URI
Especifica o local do URI de um script a ser executado.

```yaml
Type: Uri
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

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)


