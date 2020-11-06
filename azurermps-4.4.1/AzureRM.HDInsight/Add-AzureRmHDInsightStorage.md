---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
ms.openlocfilehash: f70403f70e116a0e6addc569942f927aca0dcf0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432219"
---
# <span data-ttu-id="98de5-101">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="98de5-101">Add-AzureRmHDInsightStorage</span></span>

## <span data-ttu-id="98de5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98de5-102">SYNOPSIS</span></span>
<span data-ttu-id="98de5-103">Adiciona uma chave de armazenamento do Azure a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="98de5-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98de5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98de5-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98de5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98de5-105">DESCRIPTION</span></span>
<span data-ttu-id="98de5-106">O cmdlet **Add-AzureRmHDInsightStorage** adiciona uma entrada de conta de armazenamento do Azure ao objeto de configuração do Azure HDInsight criado pelo cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="98de5-106">The **Add-AzureRmHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="98de5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98de5-107">EXAMPLES</span></span>

### <span data-ttu-id="98de5-108">Exemplo 1: adicionar uma chave de armazenamento do Azure ao objeto de configuração do cluster</span><span class="sxs-lookup"><span data-stu-id="98de5-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzureRmStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="98de5-109">Esse comando adiciona uma entrada de conta de armazenamento de blob à configuração do HDInsight chamada Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="98de5-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="98de5-110">OS</span><span class="sxs-lookup"><span data-stu-id="98de5-110">PARAMETERS</span></span>

### <span data-ttu-id="98de5-111">-Config</span><span class="sxs-lookup"><span data-stu-id="98de5-111">-Config</span></span>
<span data-ttu-id="98de5-112">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="98de5-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="98de5-113">Esse objeto é criado pelo cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="98de5-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="98de5-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="98de5-114">-StorageAccountKey</span></span>
<span data-ttu-id="98de5-115">Especifica a chave da conta de armazenamento para a qual a conta de armazenamento será adicionada ao novo cluster.</span><span class="sxs-lookup"><span data-stu-id="98de5-115">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="98de5-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="98de5-116">-StorageAccountName</span></span>
<span data-ttu-id="98de5-117">Especifica o nome da conta de armazenamento da conta de armazenamento a ser adicionada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="98de5-117">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="98de5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98de5-118">-DefaultProfile</span></span>
<span data-ttu-id="98de5-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98de5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98de5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98de5-120">CommonParameters</span></span>
<span data-ttu-id="98de5-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98de5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98de5-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98de5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98de5-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98de5-123">INPUTS</span></span>

### <span data-ttu-id="98de5-124">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="98de5-124">AzureHDInsightConfig</span></span>
<span data-ttu-id="98de5-125">O parâmetro ' config ' aceita o valor do tipo ' AzureHDInsightConfig ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="98de5-125">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="98de5-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98de5-126">OUTPUTS</span></span>

### <span data-ttu-id="98de5-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="98de5-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="98de5-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98de5-128">NOTES</span></span>

## <span data-ttu-id="98de5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98de5-129">RELATED LINKS</span></span>

[<span data-ttu-id="98de5-130">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="98de5-130">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


