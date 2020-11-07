---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 43850e035a59674b06502db1486de0d90fe6e4ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93784898"
---
# <span data-ttu-id="f6eea-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="f6eea-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="f6eea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6eea-102">SYNOPSIS</span></span>
<span data-ttu-id="f6eea-103">Adiciona uma chave de armazenamento do Azure a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="f6eea-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="f6eea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6eea-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6eea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6eea-105">DESCRIPTION</span></span>
<span data-ttu-id="f6eea-106">O cmdlet **Add-AzHDInsightStorage** adiciona uma entrada de conta de armazenamento do Azure ao objeto de configuração do Azure HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="f6eea-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f6eea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6eea-107">EXAMPLES</span></span>

### <span data-ttu-id="f6eea-108">Exemplo 1: adicionar uma chave de armazenamento do Azure ao objeto de configuração do cluster</span><span class="sxs-lookup"><span data-stu-id="f6eea-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="f6eea-109">Esse comando adiciona uma entrada de conta de armazenamento de blob à configuração do HDInsight chamada Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="f6eea-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="f6eea-110">OS</span><span class="sxs-lookup"><span data-stu-id="f6eea-110">PARAMETERS</span></span>

### <span data-ttu-id="f6eea-111">-Config</span><span class="sxs-lookup"><span data-stu-id="f6eea-111">-Config</span></span>
<span data-ttu-id="f6eea-112">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f6eea-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="f6eea-113">Esse objeto é criado pelo cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="f6eea-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6eea-114">-DefaultProfile</span></span>
<span data-ttu-id="f6eea-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f6eea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6eea-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f6eea-116">-StorageAccountKey</span></span>
<span data-ttu-id="f6eea-117">Especifica a chave da conta de armazenamento para a qual a conta de armazenamento será adicionada ao novo cluster.</span><span class="sxs-lookup"><span data-stu-id="f6eea-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f6eea-118">-StorageAccountName</span></span>
<span data-ttu-id="f6eea-119">Especifica o nome da conta de armazenamento da conta de armazenamento a ser adicionada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="f6eea-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6eea-120">CommonParameters</span></span>
<span data-ttu-id="f6eea-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6eea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6eea-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6eea-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6eea-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6eea-123">INPUTS</span></span>

### <span data-ttu-id="f6eea-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f6eea-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f6eea-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6eea-125">OUTPUTS</span></span>

### <span data-ttu-id="f6eea-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f6eea-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f6eea-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6eea-127">NOTES</span></span>

## <span data-ttu-id="f6eea-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6eea-128">RELATED LINKS</span></span>

[<span data-ttu-id="f6eea-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f6eea-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


