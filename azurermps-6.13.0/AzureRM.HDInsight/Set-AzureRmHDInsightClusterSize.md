---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: 01dfcbbc9a8996ff351ecc9d88c688c96be345d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440426"
---
# <span data-ttu-id="78fb1-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="78fb1-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="78fb1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="78fb1-103">Define o número de nós de trabalho em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="78fb1-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78fb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78fb1-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78fb1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="78fb1-106">O cmdlet **set-AzureRmHDInsightClusterSize** define o número de nós de trabalho em um cluster do Azure HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="78fb1-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="78fb1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78fb1-107">EXAMPLES</span></span>

### <span data-ttu-id="78fb1-108">Exemplo 1: definir o tamanho de um cluster especificado</span><span class="sxs-lookup"><span data-stu-id="78fb1-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="78fb1-109">Esse comando define o tamanho do cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="78fb1-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="78fb1-110">OS</span><span class="sxs-lookup"><span data-stu-id="78fb1-110">PARAMETERS</span></span>

### <span data-ttu-id="78fb1-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="78fb1-111">-ClusterName</span></span>
<span data-ttu-id="78fb1-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="78fb1-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="78fb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fb1-113">-DefaultProfile</span></span>
<span data-ttu-id="78fb1-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="78fb1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78fb1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78fb1-115">-ResourceGroupName</span></span>
<span data-ttu-id="78fb1-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78fb1-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="78fb1-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="78fb1-117">-TargetInstanceCount</span></span>
<span data-ttu-id="78fb1-118">Especifica o número desejado de nós de trabalho no cluster.</span><span class="sxs-lookup"><span data-stu-id="78fb1-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78fb1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fb1-119">CommonParameters</span></span>
<span data-ttu-id="78fb1-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78fb1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fb1-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78fb1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fb1-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78fb1-122">INPUTS</span></span>

### <span data-ttu-id="78fb1-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="78fb1-123">None</span></span>

## <span data-ttu-id="78fb1-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78fb1-124">OUTPUTS</span></span>

### <span data-ttu-id="78fb1-125">Microsoft. Azure. Management. HDInsight. Models. cluster</span><span class="sxs-lookup"><span data-stu-id="78fb1-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="78fb1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78fb1-126">NOTES</span></span>

## <span data-ttu-id="78fb1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78fb1-127">RELATED LINKS</span></span>
