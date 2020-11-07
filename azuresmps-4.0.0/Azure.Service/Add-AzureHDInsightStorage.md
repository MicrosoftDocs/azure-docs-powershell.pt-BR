---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945716"
---
# <span data-ttu-id="a2ab2-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a2ab2-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="a2ab2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ab2-103">Adiciona uma entrada de conta de armazenamento de blob a uma configuração do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="a2ab2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2ab2-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2ab2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2ab2-105">DESCRIPTION</span></span>
<span data-ttu-id="a2ab2-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="a2ab2-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="a2ab2-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="a2ab2-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="a2ab2-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="a2ab2-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="a2ab2-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="a2ab2-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a2ab2-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="a2ab2-112">O cmdlet **Add-AzureHDInsightStorage** adiciona uma entrada de conta de armazenamento blob a uma configuração do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="a2ab2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2ab2-113">EXAMPLES</span></span>

### <span data-ttu-id="a2ab2-114">Exemplo 1: adicionar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a2ab2-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="a2ab2-115">Esse comando adiciona uma conta de armazenamento chamada mystorage ao objeto de configuração armazenado no $Config e, em seguida, armazena a configuração na variável $StoreConfig.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="a2ab2-116">Exemplo 2: configurar várias contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a2ab2-116">Example 2: Configure multiple storage accounts</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="a2ab2-117">O primeiro comando usa o cmdlet **Get-AzureSubscription** para obter a ID de assinatura atual e, em seguida, armazena-a na variável $SubId.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="a2ab2-118">O segundo e terceiro comandos usam o cmdlet **Get-AzureStorageKey** para obter as chaves de armazenamento principal para MyBlobStorage e MySecondBlobStorage e, em seguida, armazenar as chaves nas variáveis $Key 1 e $Key 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="a2ab2-119">Os comandos quarto, quinto e sexto recebem credenciais para a assinatura atual e para Oozie e Hive e armazenam as credenciais em variáveis.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="a2ab2-120">O comando final executa uma sequência de operações usando estes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a2ab2-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="a2ab2-121">**New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="a2ab2-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="a2ab2-122">**Set-AzureHDInsightDefaultStorage** para definir a conta de armazenamento padrão para a configuração como MyBlobStorage.blob.Core.Windows.net</span><span class="sxs-lookup"><span data-stu-id="a2ab2-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="a2ab2-123">**Add-AzureHDInsightStorage** para adicionar uma segunda conta de armazenamento chamada MySecondBlobStorage.blob.Core.Windows.net à configuração</span><span class="sxs-lookup"><span data-stu-id="a2ab2-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="a2ab2-124">**Add-AzureHDInsightStorage** para adicionar um metastore para Oozie e um metastore para Hive à configuração</span><span class="sxs-lookup"><span data-stu-id="a2ab2-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="a2ab2-125">**New-AzureHDInsightCluster** para criar um cluster HDInsight com a nova configuração</span><span class="sxs-lookup"><span data-stu-id="a2ab2-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="a2ab2-126">OS</span><span class="sxs-lookup"><span data-stu-id="a2ab2-126">PARAMETERS</span></span>

### <span data-ttu-id="a2ab2-127">-Config</span><span class="sxs-lookup"><span data-stu-id="a2ab2-127">-Config</span></span>
<span data-ttu-id="a2ab2-128">Especifica um objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-128">Specifies a configuration object.</span></span>
<span data-ttu-id="a2ab2-129">Esse cmdlet adiciona informações da conta de armazenamento ao objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2ab2-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a2ab2-130">-Profile</span></span>
<span data-ttu-id="a2ab2-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2ab2-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2ab2-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a2ab2-133">-StorageAccountKey</span></span>
<span data-ttu-id="a2ab2-134">Especifica a chave da conta de armazenamento usada para acessar uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="a2ab2-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a2ab2-135">-StorageAccountName</span></span>
<span data-ttu-id="a2ab2-136">Especifica o nome da conta de armazenamento do Azure a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="a2ab2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ab2-137">CommonParameters</span></span>
<span data-ttu-id="a2ab2-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ab2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ab2-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ab2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ab2-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2ab2-140">INPUTS</span></span>

## <span data-ttu-id="a2ab2-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2ab2-141">OUTPUTS</span></span>

## <span data-ttu-id="a2ab2-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2ab2-142">NOTES</span></span>

## <span data-ttu-id="a2ab2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2ab2-143">RELATED LINKS</span></span>

[<span data-ttu-id="a2ab2-144">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a2ab2-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="a2ab2-145">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a2ab2-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="a2ab2-146">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="a2ab2-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


