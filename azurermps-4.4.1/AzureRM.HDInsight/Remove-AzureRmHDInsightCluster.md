---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: a09da5122403d971d8b5d1abde79c8a9a95c3ecd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440662"
---
# <span data-ttu-id="a67da-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a67da-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="a67da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a67da-102">SYNOPSIS</span></span>
<span data-ttu-id="a67da-103">Remove o cluster HDInsight especificado da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a67da-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a67da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a67da-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a67da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a67da-105">DESCRIPTION</span></span>
<span data-ttu-id="a67da-106">O cmdlet **Remove-AzureRmHDInsightCluster** remove o cluster de serviço HDInsight especificado de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a67da-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="a67da-107">Essa operação também exclui todos os dados armazenados no Hadoop (sistema de arquivos distribuído) Hadoop no cluster.</span><span class="sxs-lookup"><span data-stu-id="a67da-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="a67da-108">Os dados armazenados na conta de armazenamento associada ao Azure não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="a67da-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="a67da-109">Os dados armazenados em metarepositórios externos não são excluídos.</span><span class="sxs-lookup"><span data-stu-id="a67da-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="a67da-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a67da-110">EXAMPLES</span></span>

### <span data-ttu-id="a67da-111">Exemplo 1: excluir um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="a67da-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a67da-112">Esse comando Remove o cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a67da-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a67da-113">OS</span><span class="sxs-lookup"><span data-stu-id="a67da-113">PARAMETERS</span></span>

### <span data-ttu-id="a67da-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a67da-114">-ClusterName</span></span>
<span data-ttu-id="a67da-115">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a67da-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a67da-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67da-116">-ResourceGroupName</span></span>
<span data-ttu-id="a67da-117">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a67da-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a67da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67da-118">-DefaultProfile</span></span>
<span data-ttu-id="a67da-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a67da-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a67da-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67da-120">CommonParameters</span></span>
<span data-ttu-id="a67da-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67da-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67da-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a67da-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67da-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a67da-123">INPUTS</span></span>

## <span data-ttu-id="a67da-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a67da-124">OUTPUTS</span></span>

### <span data-ttu-id="a67da-125">Microsoft. Azure. Management. HDInsight. Models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="a67da-125">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="a67da-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a67da-126">NOTES</span></span>

## <span data-ttu-id="a67da-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a67da-127">RELATED LINKS</span></span>

[<span data-ttu-id="a67da-128">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a67da-128">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="a67da-129">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a67da-129">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


