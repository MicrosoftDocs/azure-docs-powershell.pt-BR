---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: 180cf2082b17e16fe5efcf1ee3009256b7c4703c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610502"
---
# <span data-ttu-id="1e6c7-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="1e6c7-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="1e6c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e6c7-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6c7-103">Define o número de nós de trabalho em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="1e6c7-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e6c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e6c7-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e6c7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e6c7-105">DESCRIPTION</span></span>
<span data-ttu-id="1e6c7-106">O cmdlet **set-AzureRmHDInsightClusterSize** define o número de nós de trabalho em um cluster do Azure HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="1e6c7-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1e6c7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e6c7-107">EXAMPLES</span></span>

### <span data-ttu-id="1e6c7-108">Exemplo 1: definir o tamanho de um cluster especificado</span><span class="sxs-lookup"><span data-stu-id="1e6c7-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="1e6c7-109">Esse comando define o tamanho do cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="1e6c7-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="1e6c7-110">OS</span><span class="sxs-lookup"><span data-stu-id="1e6c7-110">PARAMETERS</span></span>

### <span data-ttu-id="1e6c7-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1e6c7-111">-ClusterName</span></span>
<span data-ttu-id="1e6c7-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="1e6c7-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="1e6c7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6c7-113">-ResourceGroupName</span></span>
<span data-ttu-id="1e6c7-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e6c7-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1e6c7-115">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="1e6c7-115">-TargetInstanceCount</span></span>
<span data-ttu-id="1e6c7-116">Especifica o número desejado de nós de trabalho no cluster.</span><span class="sxs-lookup"><span data-stu-id="1e6c7-116">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="1e6c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c7-117">-DefaultProfile</span></span>
<span data-ttu-id="1e6c7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6c7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e6c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6c7-119">CommonParameters</span></span>
<span data-ttu-id="1e6c7-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6c7-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6c7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6c7-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e6c7-122">INPUTS</span></span>

## <span data-ttu-id="1e6c7-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e6c7-123">OUTPUTS</span></span>

### <span data-ttu-id="1e6c7-124">Microsoft. Azure. Management. HDInsight. Models. cluster</span><span class="sxs-lookup"><span data-stu-id="1e6c7-124">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="1e6c7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e6c7-125">NOTES</span></span>

## <span data-ttu-id="1e6c7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e6c7-126">RELATED LINKS</span></span>

