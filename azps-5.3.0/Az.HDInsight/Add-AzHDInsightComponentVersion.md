---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: ae8d096da4a21b3f53efcd14fc28b19bd133b369
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429318"
---
# <span data-ttu-id="d8c07-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="d8c07-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="d8c07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8c07-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c07-103">Adiciona uma versão de um serviço em execução em um cluster a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="d8c07-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="d8c07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8c07-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8c07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8c07-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c07-106">O cmdlet Add-AzHDInsightComponentVersion adiciona uma versão de um serviço em execução em um cluster ao objeto de configuração do Azure HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d8c07-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="d8c07-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8c07-107">EXAMPLES</span></span>

### <span data-ttu-id="d8c07-108">Exemplo 1: adicionar uma versão para Spark ao objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="d8c07-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightClusterConfig `
            | Add-AzHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="d8c07-109">Esse comando adiciona a versão do Spark ao cluster HDInsight chamado ' a-faísca-001 '.</span><span class="sxs-lookup"><span data-stu-id="d8c07-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="d8c07-110">OS</span><span class="sxs-lookup"><span data-stu-id="d8c07-110">PARAMETERS</span></span>

### <span data-ttu-id="d8c07-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="d8c07-111">-ComponentName</span></span>
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

### <span data-ttu-id="d8c07-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="d8c07-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="d8c07-113">-Config</span><span class="sxs-lookup"><span data-stu-id="d8c07-113">-Config</span></span>
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

### <span data-ttu-id="d8c07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c07-114">-DefaultProfile</span></span>
<span data-ttu-id="d8c07-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d8c07-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8c07-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8c07-116">-Confirm</span></span>
<span data-ttu-id="d8c07-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8c07-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c07-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c07-118">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c07-119">CommonParameters</span></span>
<span data-ttu-id="d8c07-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c07-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8c07-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c07-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8c07-122">INPUTS</span></span>

### <span data-ttu-id="d8c07-123">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d8c07-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d8c07-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8c07-124">OUTPUTS</span></span>

### <span data-ttu-id="d8c07-125">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d8c07-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d8c07-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8c07-126">NOTES</span></span>

## <span data-ttu-id="d8c07-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8c07-127">RELATED LINKS</span></span>
