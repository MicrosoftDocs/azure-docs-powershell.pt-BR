---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 868ab69420cac66e911d772f4362e70ec2c03a1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942796"
---
# <span data-ttu-id="4a5f2-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="4a5f2-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="4a5f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a5f2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5f2-103">Adiciona uma versão de um serviço em execução em um cluster a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="4a5f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a5f2-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a5f2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a5f2-105">DESCRIPTION</span></span>
<span data-ttu-id="4a5f2-106">O cmdlet Add-AzHDInsightComponentVersion adiciona uma versão de um serviço em execução em um cluster ao objeto de configuração do Azure HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4a5f2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a5f2-107">EXAMPLES</span></span>

### <span data-ttu-id="4a5f2-108">Exemplo 1: adicionar uma versão para Spark ao objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="4a5f2-109">Esse comando adiciona a versão do Spark ao cluster HDInsight chamado ' a-faísca-001 '.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="4a5f2-110">OS</span><span class="sxs-lookup"><span data-stu-id="4a5f2-110">PARAMETERS</span></span>

### <span data-ttu-id="4a5f2-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="4a5f2-111">-ComponentName</span></span>
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

### <span data-ttu-id="4a5f2-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="4a5f2-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="4a5f2-113">-Config</span><span class="sxs-lookup"><span data-stu-id="4a5f2-113">-Config</span></span>
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

### <span data-ttu-id="4a5f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5f2-114">-DefaultProfile</span></span>
<span data-ttu-id="4a5f2-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4a5f2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a5f2-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a5f2-116">-Confirm</span></span>
<span data-ttu-id="4a5f2-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a5f2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a5f2-118">-WhatIf</span></span>
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

### <span data-ttu-id="4a5f2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5f2-119">CommonParameters</span></span>
<span data-ttu-id="4a5f2-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a5f2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5f2-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a5f2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5f2-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a5f2-122">INPUTS</span></span>

### <span data-ttu-id="4a5f2-123">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4a5f2-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4a5f2-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a5f2-124">OUTPUTS</span></span>

### <span data-ttu-id="4a5f2-125">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4a5f2-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4a5f2-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a5f2-126">NOTES</span></span>

## <span data-ttu-id="4a5f2-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a5f2-127">RELATED LINKS</span></span>
