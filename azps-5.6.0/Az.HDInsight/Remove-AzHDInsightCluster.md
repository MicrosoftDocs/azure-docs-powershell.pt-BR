---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: 5baf67bfec2c4e18e718241dbb973bb8b2050bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887123"
---
# <span data-ttu-id="5105a-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5105a-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="5105a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5105a-102">SYNOPSIS</span></span>
<span data-ttu-id="5105a-103">Remove o cluster HDInsight especificado da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="5105a-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="5105a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5105a-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5105a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5105a-105">DESCRIPTION</span></span>
<span data-ttu-id="5105a-106">O cmdlet **Remove-AzHDInsightCluster** remove o cluster de serviço HDInsight especificado de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5105a-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="5105a-107">Essa operação também exclui todos os dados armazenados no Sistema de Arquivos Distribuídos Hadoop (HDFS) no cluster.</span><span class="sxs-lookup"><span data-stu-id="5105a-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="5105a-108">Os dados armazenados na conta de Armazenamento do Azure associada não são excluídos.</span><span class="sxs-lookup"><span data-stu-id="5105a-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="5105a-109">Os dados armazenados em metadadores externos não são excluídos.</span><span class="sxs-lookup"><span data-stu-id="5105a-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="5105a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5105a-110">EXAMPLES</span></span>

### <span data-ttu-id="5105a-111">Exemplo 1: Excluir um cluster HDInsight do Azure</span><span class="sxs-lookup"><span data-stu-id="5105a-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="5105a-112">Este comando remove o cluster chamado your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="5105a-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5105a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5105a-113">PARAMETERS</span></span>

### <span data-ttu-id="5105a-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5105a-114">-ClusterName</span></span>
<span data-ttu-id="5105a-115">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="5105a-115">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5105a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5105a-116">-DefaultProfile</span></span>
<span data-ttu-id="5105a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5105a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5105a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5105a-118">-PassThru</span></span>
<span data-ttu-id="5105a-119">Se PassThru estiver presente, resulte no resultado</span><span class="sxs-lookup"><span data-stu-id="5105a-119">If PassThru is present, output the result</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5105a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5105a-120">-ResourceGroupName</span></span>
<span data-ttu-id="5105a-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5105a-121">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5105a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5105a-122">CommonParameters</span></span>
<span data-ttu-id="5105a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5105a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5105a-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5105a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5105a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5105a-125">INPUTS</span></span>

### <span data-ttu-id="5105a-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5105a-126">None</span></span>
## <span data-ttu-id="5105a-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5105a-127">OUTPUTS</span></span>

### <span data-ttu-id="5105a-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5105a-128">System.Boolean</span></span>
## <span data-ttu-id="5105a-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="5105a-129">NOTES</span></span>

## <span data-ttu-id="5105a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5105a-130">RELATED LINKS</span></span>

[<span data-ttu-id="5105a-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5105a-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="5105a-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5105a-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


