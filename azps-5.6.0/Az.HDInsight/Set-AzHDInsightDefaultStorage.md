---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 9873ba2e4fa4f54c4aa77822af076bb5426ac198
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891841"
---
# <span data-ttu-id="ff3f4-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="ff3f4-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="ff3f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3f4-103">Define a configuração padrão da conta de armazenamento em um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="ff3f4-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="ff3f4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ff3f4-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountResourceId] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff3f4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ff3f4-105">DESCRIPTION</span></span>
<span data-ttu-id="ff3f4-106">O cmdlet **Set-AzHDInsightDefaultStorage** define a configuração da conta de armazenamento padrão no objeto de configuração de cluster HDInsight do Azure criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ff3f4-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ff3f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff3f4-107">EXAMPLES</span></span>

### <span data-ttu-id="ff3f4-108">Exemplo 1: definir a conta de armazenamento padrão para o objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="ff3f4-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
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

<span data-ttu-id="ff3f4-109">Este comando define a conta de armazenamento padrão para um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="ff3f4-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="ff3f4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ff3f4-110">PARAMETERS</span></span>

### <span data-ttu-id="ff3f4-111">-Config</span><span class="sxs-lookup"><span data-stu-id="ff3f4-111">-Config</span></span>
<span data-ttu-id="ff3f4-112">Especifica o objeto de configuração de cluster HDInsight que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ff3f4-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ff3f4-113">Esse objeto é criado pelo cmdlet **New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="ff3f4-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="ff3f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3f4-114">-DefaultProfile</span></span>
<span data-ttu-id="ff3f4-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ff3f4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff3f4-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff3f4-116">-StorageAccountKey</span></span>
<span data-ttu-id="ff3f4-117">Especifica a chave de conta da conta padrão do Armazenamento do Azure que o cluster HDInsight usará.</span><span class="sxs-lookup"><span data-stu-id="ff3f4-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="ff3f4-118">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ff3f4-118">-StorageAccountResourceId</span></span>
<span data-ttu-id="ff3f4-119">O nome da conta de armazenamento para a conta de armazenamento a ser adicionada ao novo cluster.</span><span class="sxs-lookup"><span data-stu-id="ff3f4-119">The storage account name for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="ff3f4-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ff3f4-120">-StorageAccountType</span></span>
<span data-ttu-id="ff3f4-121">Obtém ou define o tipo da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="ff3f4-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="ff3f4-122">Padrões para AzureStorage</span><span class="sxs-lookup"><span data-stu-id="ff3f4-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3f4-123">CommonParameters</span></span>
<span data-ttu-id="ff3f4-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff3f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3f4-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff3f4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3f4-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff3f4-126">INPUTS</span></span>

### <span data-ttu-id="ff3f4-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ff3f4-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ff3f4-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ff3f4-128">OUTPUTS</span></span>

### <span data-ttu-id="ff3f4-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ff3f4-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ff3f4-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="ff3f4-130">NOTES</span></span>

## <span data-ttu-id="ff3f4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff3f4-131">RELATED LINKS</span></span>
