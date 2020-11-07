---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: e4ecdb86d3c8b055f76303af5c3b86fc9813e167
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955572"
---
# <span data-ttu-id="40162-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="40162-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="40162-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40162-102">SYNOPSIS</span></span>
<span data-ttu-id="40162-103">Define a configuração da conta de armazenamento padrão em um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="40162-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="40162-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40162-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40162-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40162-105">DESCRIPTION</span></span>
<span data-ttu-id="40162-106">O cmdlet **set-AzHDInsightDefaultStorage** define a configuração padrão da conta de armazenamento no objeto de configuração do cluster do Azure HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="40162-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="40162-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40162-107">EXAMPLES</span></span>

### <span data-ttu-id="40162-108">Exemplo 1: definir a conta de armazenamento padrão para o objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="40162-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="40162-109">Esse comando define a conta de armazenamento padrão para um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="40162-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="40162-110">OS</span><span class="sxs-lookup"><span data-stu-id="40162-110">PARAMETERS</span></span>

### <span data-ttu-id="40162-111">-Config</span><span class="sxs-lookup"><span data-stu-id="40162-111">-Config</span></span>
<span data-ttu-id="40162-112">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="40162-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="40162-113">Esse objeto é criado pelo cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="40162-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="40162-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40162-114">-DefaultProfile</span></span>
<span data-ttu-id="40162-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="40162-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40162-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="40162-116">-StorageAccountKey</span></span>
<span data-ttu-id="40162-117">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="40162-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40162-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="40162-118">-StorageAccountName</span></span>
<span data-ttu-id="40162-119">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="40162-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="40162-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="40162-120">-StorageAccountType</span></span>
<span data-ttu-id="40162-121">Obtém ou define o tipo da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="40162-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="40162-122">Padrões para AzureStorage</span><span class="sxs-lookup"><span data-stu-id="40162-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40162-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40162-123">CommonParameters</span></span>
<span data-ttu-id="40162-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40162-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40162-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40162-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40162-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40162-126">INPUTS</span></span>

### <span data-ttu-id="40162-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="40162-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="40162-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40162-128">OUTPUTS</span></span>

### <span data-ttu-id="40162-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="40162-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="40162-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40162-130">NOTES</span></span>

## <span data-ttu-id="40162-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40162-131">RELATED LINKS</span></span>
