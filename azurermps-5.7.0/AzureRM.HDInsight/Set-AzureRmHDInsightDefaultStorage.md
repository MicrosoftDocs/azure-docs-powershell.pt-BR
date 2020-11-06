---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: 43418937c379ba1ac93b5a2c733028e31eef7318
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602860"
---
# <span data-ttu-id="04feb-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="04feb-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="04feb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04feb-102">SYNOPSIS</span></span>
<span data-ttu-id="04feb-103">Define a configuração da conta de armazenamento padrão em um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="04feb-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04feb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04feb-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04feb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04feb-105">DESCRIPTION</span></span>
<span data-ttu-id="04feb-106">O cmdlet **set-AzureRmHDInsightDefaultStorage** define a configuração padrão da conta de armazenamento no objeto de configuração do cluster do Azure HDInsight criado pelo cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="04feb-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="04feb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04feb-107">EXAMPLES</span></span>

### <span data-ttu-id="04feb-108">Exemplo 1: definir a conta de armazenamento padrão para o objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="04feb-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="04feb-109">Esse comando define a conta de armazenamento padrão para um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="04feb-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="04feb-110">OS</span><span class="sxs-lookup"><span data-stu-id="04feb-110">PARAMETERS</span></span>

### <span data-ttu-id="04feb-111">-Config</span><span class="sxs-lookup"><span data-stu-id="04feb-111">-Config</span></span>
<span data-ttu-id="04feb-112">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="04feb-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="04feb-113">Esse objeto é criado pelo cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="04feb-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04feb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04feb-114">-DefaultProfile</span></span>
<span data-ttu-id="04feb-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="04feb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04feb-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="04feb-116">-StorageAccountKey</span></span>
<span data-ttu-id="04feb-117">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="04feb-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04feb-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04feb-118">-StorageAccountName</span></span>
<span data-ttu-id="04feb-119">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="04feb-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04feb-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="04feb-120">-StorageAccountType</span></span>
<span data-ttu-id="04feb-121">Obtém ou define o tipo da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="04feb-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="04feb-122">Padrões para AzureStorage</span><span class="sxs-lookup"><span data-stu-id="04feb-122">Defaults to AzureStorage</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04feb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04feb-123">CommonParameters</span></span>
<span data-ttu-id="04feb-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04feb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04feb-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04feb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04feb-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04feb-126">INPUTS</span></span>

### <span data-ttu-id="04feb-127">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="04feb-127">AzureHDInsightConfig</span></span>
<span data-ttu-id="04feb-128">O parâmetro ' config ' aceita o valor do tipo ' AzureHDInsightConfig ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="04feb-128">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="04feb-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04feb-129">OUTPUTS</span></span>

### <span data-ttu-id="04feb-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="04feb-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="04feb-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04feb-131">NOTES</span></span>

## <span data-ttu-id="04feb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04feb-132">RELATED LINKS</span></span>

