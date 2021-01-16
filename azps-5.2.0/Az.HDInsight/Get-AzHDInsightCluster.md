---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257236"
---
# <span data-ttu-id="99862-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="99862-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="99862-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99862-102">SYNOPSIS</span></span>
<span data-ttu-id="99862-103">Obtém e lista todos os clusters do Azure HDInsight associados à assinatura atual ou um grupo de recursos especificado ou recupera um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="99862-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="99862-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99862-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99862-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99862-105">DESCRIPTION</span></span>
<span data-ttu-id="99862-106">O cmdlet **Get-AzHDInsightCluster** lista os clusters de serviço do Azure HDInsight para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="99862-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="99862-107">Use o parâmetro *ClusterName* para obter detalhes de um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="99862-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="99862-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99862-108">EXAMPLES</span></span>

### <span data-ttu-id="99862-109">Exemplo 1: listar todos os clusters do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="99862-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="99862-110">Esse comando lista todos os clusters do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="99862-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="99862-111">OS</span><span class="sxs-lookup"><span data-stu-id="99862-111">PARAMETERS</span></span>

### <span data-ttu-id="99862-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="99862-112">-ClusterName</span></span>
<span data-ttu-id="99862-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="99862-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="99862-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99862-114">-DefaultProfile</span></span>
<span data-ttu-id="99862-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="99862-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99862-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99862-116">-ResourceGroupName</span></span>
<span data-ttu-id="99862-117">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="99862-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="99862-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99862-118">CommonParameters</span></span>
<span data-ttu-id="99862-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99862-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99862-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99862-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99862-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99862-121">INPUTS</span></span>

### <span data-ttu-id="99862-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="99862-122">None</span></span>

## <span data-ttu-id="99862-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99862-123">OUTPUTS</span></span>

### <span data-ttu-id="99862-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="99862-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="99862-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99862-125">NOTES</span></span>

## <span data-ttu-id="99862-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99862-126">RELATED LINKS</span></span>

[<span data-ttu-id="99862-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="99862-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="99862-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="99862-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


