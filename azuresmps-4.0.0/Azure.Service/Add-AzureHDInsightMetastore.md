---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945723"
---
# <span data-ttu-id="cd105-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="cd105-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="cd105-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd105-102">SYNOPSIS</span></span>
<span data-ttu-id="cd105-103">Adiciona uma conta de banco de dados do SQL Server a uma configuração de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cd105-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="cd105-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd105-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd105-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd105-105">DESCRIPTION</span></span>
<span data-ttu-id="cd105-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="cd105-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="cd105-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="cd105-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="cd105-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cd105-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="cd105-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="cd105-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="cd105-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="cd105-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="cd105-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cd105-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="cd105-112">O cmdlet **Add-AzureHDInsightMetastore** adiciona um banco de dados do Microsoft SQL Server a uma configuração do Azure HDInsight que é criada pelo cmdlet **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="cd105-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="cd105-113">O banco de dados é usado para armazenar metadados para Hive ou Oozie, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="cd105-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="cd105-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd105-114">EXAMPLES</span></span>

### <span data-ttu-id="cd105-115">Exemplo 1: adicionar uma metaloja</span><span class="sxs-lookup"><span data-stu-id="cd105-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="cd105-116">Esse comando adiciona um banco de dados SQL Server chamado ContosoSQLServer para servir como um metarepositório de Hive para um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cd105-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="cd105-117">Exemplo 2: configurar armazenamento e adicionar metastores</span><span class="sxs-lookup"><span data-stu-id="cd105-117">Example 2: Configure storage and add metastores</span></span>
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

<span data-ttu-id="cd105-118">O primeiro comando usa o cmdlet **Get-AzureSubscription** para obter a ID de assinatura atual e, em seguida, armazena-a na variável $SubId.</span><span class="sxs-lookup"><span data-stu-id="cd105-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="cd105-119">O segundo e terceiro comandos usam o cmdlet **Get-AzureStorageKey** para obter as chaves de armazenamento principal para MyBlobStorage e MySecondBlobStorage e, em seguida, armazenar as chaves nas variáveis $Key 1 e $Key 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cd105-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="cd105-120">Os comandos quarto, quinto e sexto usam o cmdlet **Get-Credential** para obter credenciais para a assinatura atual e para Oozie e Hive e, em seguida, armazenar as credenciais em variáveis.</span><span class="sxs-lookup"><span data-stu-id="cd105-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="cd105-121">O comando final executa uma sequência de operações usando estes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd105-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="cd105-122">**New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cd105-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="cd105-123">**Set-AzureHDInsightDefaultStorage** para definir a conta de armazenamento padrão para a configuração para MyBlobStorage.blob.Core.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="cd105-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="cd105-124">**Add-AzureHDInsightStorage** para adicionar uma segunda conta de armazenamento chamada MySecondBlobStorage.blob.Core.Windows.net à configuração.</span><span class="sxs-lookup"><span data-stu-id="cd105-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="cd105-125">**Add-AzureHDInsightMetastore** para adicionar um metastore para Oozie e um metastore para Hive à configuração.</span><span class="sxs-lookup"><span data-stu-id="cd105-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="cd105-126">**New-AzureHDInsightCluster** para criar um cluster HDInsight com a nova configuração.</span><span class="sxs-lookup"><span data-stu-id="cd105-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="cd105-127">OS</span><span class="sxs-lookup"><span data-stu-id="cd105-127">PARAMETERS</span></span>

### <span data-ttu-id="cd105-128">-Config</span><span class="sxs-lookup"><span data-stu-id="cd105-128">-Config</span></span>
<span data-ttu-id="cd105-129">Especifica um objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="cd105-129">Specifies a configuration object.</span></span>
<span data-ttu-id="cd105-130">Esse cmdlet adiciona informações de metastore ao objeto de configuração que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="cd105-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd105-131">-Credential</span><span class="sxs-lookup"><span data-stu-id="cd105-131">-Credential</span></span>
<span data-ttu-id="cd105-132">Especifica as credenciais que são usadas para acessar um banco de dados do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cd105-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd105-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd105-133">-DatabaseName</span></span>
<span data-ttu-id="cd105-134">Especifica o nome do banco de dados para armazenar os metadados Hive ou Oozie.</span><span class="sxs-lookup"><span data-stu-id="cd105-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

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

### <span data-ttu-id="cd105-135">-Metastoretype</span><span class="sxs-lookup"><span data-stu-id="cd105-135">-MetastoreType</span></span>
<span data-ttu-id="cd105-136">Especifica o tipo de metarepositório.</span><span class="sxs-lookup"><span data-stu-id="cd105-136">Specifies the metastore type.</span></span>
<span data-ttu-id="cd105-137">Os valores aceitáveis para esse parâmetro são: HiveMetaStore ou OozieMetaStore.</span><span class="sxs-lookup"><span data-stu-id="cd105-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd105-138">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cd105-138">-Profile</span></span>
<span data-ttu-id="cd105-139">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="cd105-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd105-140">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="cd105-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd105-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="cd105-141">-SqlAzureServerName</span></span>
<span data-ttu-id="cd105-142">Especifica o nome de domínio totalmente qualificado (FQDN) do SQL Server que contém o banco de dados para armazenar metadados.</span><span class="sxs-lookup"><span data-stu-id="cd105-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

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

### <span data-ttu-id="cd105-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd105-143">CommonParameters</span></span>
<span data-ttu-id="cd105-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd105-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd105-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd105-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd105-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd105-146">INPUTS</span></span>

## <span data-ttu-id="cd105-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd105-147">OUTPUTS</span></span>

## <span data-ttu-id="cd105-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd105-148">NOTES</span></span>

## <span data-ttu-id="cd105-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd105-149">RELATED LINKS</span></span>

[<span data-ttu-id="cd105-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="cd105-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="cd105-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cd105-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="cd105-152">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="cd105-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="cd105-153">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="cd105-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
