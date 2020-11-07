---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955005"
---
# <span data-ttu-id="0b2f3-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0b2f3-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="0b2f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2f3-103">Remove o cluster HDInsight especificado da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0b2f3-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="0b2f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b2f3-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b2f3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b2f3-105">DESCRIPTION</span></span>
<span data-ttu-id="0b2f3-106">O cmdlet **Remove-AzHDInsightCluster** remove o cluster de serviço HDInsight especificado de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0b2f3-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="0b2f3-107">Essa operação também exclui todos os dados armazenados no Hadoop (sistema de arquivos distribuído) Hadoop no cluster.</span><span class="sxs-lookup"><span data-stu-id="0b2f3-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="0b2f3-108">Os dados armazenados na conta de armazenamento associada ao Azure não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="0b2f3-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="0b2f3-109">Os dados armazenados em metarepositórios externos não são excluídos.</span><span class="sxs-lookup"><span data-stu-id="0b2f3-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="0b2f3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b2f3-110">EXAMPLES</span></span>

### <span data-ttu-id="0b2f3-111">Exemplo 1: excluir um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="0b2f3-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="0b2f3-112">Esse comando Remove o cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="0b2f3-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0b2f3-113">OS</span><span class="sxs-lookup"><span data-stu-id="0b2f3-113">PARAMETERS</span></span>

### <span data-ttu-id="0b2f3-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0b2f3-114">-ClusterName</span></span>
<span data-ttu-id="0b2f3-115">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="0b2f3-115">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2f3-116">-DefaultProfile</span></span>
<span data-ttu-id="0b2f3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0b2f3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="0b2f3-119">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b2f3-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b2f3-120">-PassThru</span></span>
<span data-ttu-id="0b2f3-121">Se PassThru estiver presente, produzirá o resultado</span><span class="sxs-lookup"><span data-stu-id="0b2f3-121">If PassThru is present, output the result</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2f3-122">CommonParameters</span></span>
<span data-ttu-id="0b2f3-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2f3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2f3-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b2f3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2f3-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b2f3-125">INPUTS</span></span>

### <span data-ttu-id="0b2f3-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0b2f3-126">None</span></span>
## <span data-ttu-id="0b2f3-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b2f3-127">OUTPUTS</span></span>

### <span data-ttu-id="0b2f3-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b2f3-128">System.Boolean</span></span>
## <span data-ttu-id="0b2f3-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b2f3-129">NOTES</span></span>

## <span data-ttu-id="0b2f3-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b2f3-130">RELATED LINKS</span></span>

[<span data-ttu-id="0b2f3-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0b2f3-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="0b2f3-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0b2f3-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


