---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 6db3c5b5d899f9b7a32e6dbb20c280590bea93c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111867"
---
# <span data-ttu-id="62639-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="62639-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="62639-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62639-102">SYNOPSIS</span></span>
<span data-ttu-id="62639-103">Adiciona uma chave de Armazenamento do Azure a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="62639-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="62639-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62639-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62639-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="62639-105">DESCRIPTION</span></span>
<span data-ttu-id="62639-106">O cmdlet **Add-AzHDInsightStorage** adiciona uma entrada de conta de Armazenamento do Azure ao objeto de configuração HDInsight do Azure criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="62639-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="62639-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62639-107">EXAMPLES</span></span>

### <span data-ttu-id="62639-108">Exemplo 1: Adicionar uma chave de armazenamento do Azure ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="62639-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="62639-109">Esse comando adiciona uma entrada de conta de armazenamento de blob à configuração HDInsight chamada hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="62639-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="62639-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62639-110">PARAMETERS</span></span>

### <span data-ttu-id="62639-111">-Configuração</span><span class="sxs-lookup"><span data-stu-id="62639-111">-Config</span></span>
<span data-ttu-id="62639-112">Especifica o objeto de configuração de cluster HDInsight que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="62639-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="62639-113">Este objeto é criado pelo **cmdlet New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="62639-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="62639-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62639-114">-DefaultProfile</span></span>
<span data-ttu-id="62639-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="62639-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62639-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="62639-116">-StorageAccountKey</span></span>
<span data-ttu-id="62639-117">Especifica a chave da conta de armazenamento para que a conta de armazenamento seja adicionada ao novo cluster.</span><span class="sxs-lookup"><span data-stu-id="62639-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="62639-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62639-118">-StorageAccountName</span></span>
<span data-ttu-id="62639-119">Especifica o nome da conta de armazenamento para a conta de armazenamento a ser adicionada ao cluster.</span><span class="sxs-lookup"><span data-stu-id="62639-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="62639-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62639-120">CommonParameters</span></span>
<span data-ttu-id="62639-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62639-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62639-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62639-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62639-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="62639-123">INPUTS</span></span>

### <span data-ttu-id="62639-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="62639-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="62639-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="62639-125">OUTPUTS</span></span>

### <span data-ttu-id="62639-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="62639-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="62639-127">Notas</span><span class="sxs-lookup"><span data-stu-id="62639-127">NOTES</span></span>

## <span data-ttu-id="62639-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62639-128">RELATED LINKS</span></span>

[<span data-ttu-id="62639-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="62639-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


