---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: ff789a04be2a6f448d4850891f368cbb7ca91c4b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93784890"
---
# <span data-ttu-id="2eec9-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2eec9-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="2eec9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2eec9-102">SYNOPSIS</span></span>
<span data-ttu-id="2eec9-103">Obtém e lista todos os clusters do Azure HDInsight associados à assinatura atual ou um grupo de recursos especificado ou recupera um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="2eec9-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="2eec9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2eec9-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eec9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2eec9-105">DESCRIPTION</span></span>
<span data-ttu-id="2eec9-106">O cmdlet **Get-AzHDInsightCluster** lista os clusters de serviço do Azure HDInsight para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="2eec9-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="2eec9-107">Use o parâmetro *ClusterName* para obter detalhes de um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="2eec9-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="2eec9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2eec9-108">EXAMPLES</span></span>

### <span data-ttu-id="2eec9-109">Exemplo 1: listar todos os clusters do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="2eec9-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="2eec9-110">Esse comando lista todos os clusters do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2eec9-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="2eec9-111">OS</span><span class="sxs-lookup"><span data-stu-id="2eec9-111">PARAMETERS</span></span>

### <span data-ttu-id="2eec9-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2eec9-112">-ClusterName</span></span>
<span data-ttu-id="2eec9-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2eec9-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eec9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eec9-114">-DefaultProfile</span></span>
<span data-ttu-id="2eec9-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2eec9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2eec9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eec9-116">-ResourceGroupName</span></span>
<span data-ttu-id="2eec9-117">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2eec9-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eec9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eec9-118">CommonParameters</span></span>
<span data-ttu-id="2eec9-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eec9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eec9-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eec9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eec9-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2eec9-121">INPUTS</span></span>

### <span data-ttu-id="2eec9-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2eec9-122">None</span></span>

## <span data-ttu-id="2eec9-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2eec9-123">OUTPUTS</span></span>

### <span data-ttu-id="2eec9-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2eec9-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="2eec9-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2eec9-125">NOTES</span></span>

## <span data-ttu-id="2eec9-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2eec9-126">RELATED LINKS</span></span>

[<span data-ttu-id="2eec9-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2eec9-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="2eec9-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2eec9-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


