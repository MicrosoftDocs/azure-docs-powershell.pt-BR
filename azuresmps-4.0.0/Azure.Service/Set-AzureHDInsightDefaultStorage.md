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
# <span data-ttu-id="e3fd6-101">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="e3fd6-101">Set-AzureHDInsightDefaultStorage</span></span>

## <span data-ttu-id="e3fd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fd6-103">Define a conta de armazenamento padrão para um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-103">Sets the default storage account for an HDInsight cluster.</span></span>

## <span data-ttu-id="e3fd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3fd6-104">SYNTAX</span></span>

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3fd6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3fd6-105">DESCRIPTION</span></span>
<span data-ttu-id="e3fd6-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e3fd6-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e3fd6-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e3fd6-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e3fd6-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e3fd6-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e3fd6-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e3fd6-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e3fd6-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e3fd6-112">O cmdlet **set-AzureHDInsightDefaultStorage** define a conta de armazenamento padrão para uma configuração de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-112">The **Set-AzureHDInsightDefaultStorage** cmdlet sets the default storage account for an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="e3fd6-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3fd6-113">EXAMPLES</span></span>

### <span data-ttu-id="e3fd6-114">Exemplo 1: definir a conta de armazenamento padrão</span><span class="sxs-lookup"><span data-stu-id="e3fd6-114">Example 1: Set the default storage account</span></span>
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

<span data-ttu-id="e3fd6-115">O primeiro comando usa o cmdlet **Get-AzureSubscription** para obter a ID de assinatura atual e, em seguida, armazena-a na variável $SubId.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="e3fd6-116">O segundo e terceiro comandos usam o cmdlet **Get-AzureStorageKey** para obter as chaves de armazenamento principal para MyBlobStorage e MySecondBlobStorage e, em seguida, armazenar as chaves nas variáveis $Key 1 e $Key 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="e3fd6-117">Os comandos quarto, quinto e sexto usam o cmdlet **Get-Credential** para obter credenciais para a assinatura atual e, em seguida, armazenam as credenciais nas variáveis $Creds, $OozieCreds e $HiveCreds.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription, and then stores the credentials in the $Creds, $OozieCreds, and $HiveCreds variables.</span></span>

<span data-ttu-id="e3fd6-118">O comando final executa uma sequência de operações usando estes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e3fd6-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="e3fd6-119">**New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="e3fd6-120">**Set-AzureHDInsightDefaultStorage** para definir a conta de armazenamento padrão para a configuração para MyBlobStorage.blob.Core.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="e3fd6-121">**Add-AzureHDInsightStorage** para adicionar uma segunda conta de armazenamento chamada MySecondBlobStorage.blob.Core.Windows.net à configuração.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="e3fd6-122">**Add-AzureHDInsightMetastore** para adicionar um metastore para Oozie e um metastore para Hive à configuração.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="e3fd6-123">**New-AzureHDInsightCluster** para criar um cluster HDInsight com a nova configuração.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="e3fd6-124">OS</span><span class="sxs-lookup"><span data-stu-id="e3fd6-124">PARAMETERS</span></span>

### <span data-ttu-id="e3fd6-125">-Config</span><span class="sxs-lookup"><span data-stu-id="e3fd6-125">-Config</span></span>
<span data-ttu-id="e3fd6-126">Especifica um objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-126">Specifies a configuration object.</span></span>
<span data-ttu-id="e3fd6-127">Esse cmdlet define a conta de armazenamento padrão para o objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-127">This cmdlet sets the default storage account for the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="e3fd6-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e3fd6-128">-Profile</span></span>
<span data-ttu-id="e3fd6-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3fd6-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3fd6-131">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e3fd6-131">-StorageAccountKey</span></span>
<span data-ttu-id="e3fd6-132">Especifica a chave da conta de armazenamento que é usada para acessar a conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-132">Specifies the storage account key that is used to access the default storage account.</span></span>

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

### <span data-ttu-id="e3fd6-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e3fd6-133">-StorageAccountName</span></span>
<span data-ttu-id="e3fd6-134">Especifica o nome de uma conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-134">Specifies the name of a default storage account.</span></span>

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

### <span data-ttu-id="e3fd6-135">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="e3fd6-135">-StorageContainerName</span></span>
<span data-ttu-id="e3fd6-136">Especifica o nome do contêiner de armazenamento padrão para um cluster.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-136">Specifies the name of the default storage container for a cluster.</span></span>

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

### <span data-ttu-id="e3fd6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fd6-137">CommonParameters</span></span>
<span data-ttu-id="e3fd6-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3fd6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fd6-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3fd6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fd6-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3fd6-140">INPUTS</span></span>

## <span data-ttu-id="e3fd6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3fd6-141">OUTPUTS</span></span>

## <span data-ttu-id="e3fd6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3fd6-142">NOTES</span></span>

## <span data-ttu-id="e3fd6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3fd6-143">RELATED LINKS</span></span>

[<span data-ttu-id="e3fd6-144">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="e3fd6-144">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="e3fd6-145">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="e3fd6-145">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="e3fd6-146">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e3fd6-146">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="e3fd6-147">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e3fd6-147">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


