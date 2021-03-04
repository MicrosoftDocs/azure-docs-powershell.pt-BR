---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: eba552917b17b9bb1337a2b62c83d3d1adebc1cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891842"
---
# <span data-ttu-id="67643-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="67643-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="67643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67643-102">SYNOPSIS</span></span>
<span data-ttu-id="67643-103">Define o número de nós De trabalho em um cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="67643-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="67643-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="67643-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67643-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="67643-105">DESCRIPTION</span></span>
<span data-ttu-id="67643-106">O cmdlet **Set-AzHDInsightClusterSize** define o número de nós do Worker em um cluster HDInsight do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="67643-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="67643-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67643-107">EXAMPLES</span></span>

### <span data-ttu-id="67643-108">Exemplo 1: definir o tamanho de um cluster especificado</span><span class="sxs-lookup"><span data-stu-id="67643-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="67643-109">Este comando define o tamanho do cluster chamado your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="67643-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="67643-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="67643-110">PARAMETERS</span></span>

### <span data-ttu-id="67643-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="67643-111">-ClusterName</span></span>
<span data-ttu-id="67643-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="67643-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="67643-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67643-113">-DefaultProfile</span></span>
<span data-ttu-id="67643-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="67643-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67643-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67643-115">-ResourceGroupName</span></span>
<span data-ttu-id="67643-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="67643-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="67643-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="67643-117">-TargetInstanceCount</span></span>
<span data-ttu-id="67643-118">Especifica o número desejado de nós de trabalho no cluster.</span><span class="sxs-lookup"><span data-stu-id="67643-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="67643-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67643-119">CommonParameters</span></span>
<span data-ttu-id="67643-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67643-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67643-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67643-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67643-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67643-122">INPUTS</span></span>

### <span data-ttu-id="67643-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="67643-123">None</span></span>

## <span data-ttu-id="67643-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="67643-124">OUTPUTS</span></span>

### <span data-ttu-id="67643-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="67643-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="67643-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="67643-126">NOTES</span></span>

## <span data-ttu-id="67643-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67643-127">RELATED LINKS</span></span>
