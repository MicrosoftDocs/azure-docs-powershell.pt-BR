---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: ae8d096da4a21b3f53efcd14fc28b19bd133b369
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126940"
---
# <span data-ttu-id="43925-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="43925-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="43925-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43925-102">SYNOPSIS</span></span>
<span data-ttu-id="43925-103">Adiciona uma versão para um serviço em execução em um cluster a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="43925-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="43925-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43925-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43925-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="43925-105">DESCRIPTION</span></span>
<span data-ttu-id="43925-106">O Add-AzHDInsightComponentVersion cmdlet adiciona uma versão para um serviço em execução em um cluster ao objeto de configuração HDInsight do Azure criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="43925-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="43925-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43925-107">EXAMPLES</span></span>

### <span data-ttu-id="43925-108">Exemplo 1: Adicionar uma versão do Spark ao objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="43925-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
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

<span data-ttu-id="43925-109">Esse comando adiciona a versão do Spark ao cluster HDInsight chamado "seu-spark-001".</span><span class="sxs-lookup"><span data-stu-id="43925-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="43925-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43925-110">PARAMETERS</span></span>

### <span data-ttu-id="43925-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="43925-111">-ComponentName</span></span>
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

### <span data-ttu-id="43925-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="43925-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="43925-113">-Configuração</span><span class="sxs-lookup"><span data-stu-id="43925-113">-Config</span></span>
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

### <span data-ttu-id="43925-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43925-114">-DefaultProfile</span></span>
<span data-ttu-id="43925-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="43925-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43925-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="43925-116">-Confirm</span></span>
<span data-ttu-id="43925-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43925-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43925-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43925-118">-WhatIf</span></span>
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

### <span data-ttu-id="43925-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43925-119">CommonParameters</span></span>
<span data-ttu-id="43925-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43925-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43925-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43925-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43925-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="43925-122">INPUTS</span></span>

### <span data-ttu-id="43925-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="43925-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="43925-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="43925-124">OUTPUTS</span></span>

### <span data-ttu-id="43925-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="43925-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="43925-126">Notas</span><span class="sxs-lookup"><span data-stu-id="43925-126">NOTES</span></span>

## <span data-ttu-id="43925-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43925-127">RELATED LINKS</span></span>
