---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: c89293ee071aba3fcec2d58d071714193cc44a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892962"
---
# <span data-ttu-id="cbc3f-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cbc3f-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="cbc3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbc3f-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc3f-103">Obtém e lista todos os clusters HDInsight do Azure associados à assinatura atual ou a um grupo de recursos especificado ou recupera um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="cbc3f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cbc3f-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbc3f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cbc3f-105">DESCRIPTION</span></span>
<span data-ttu-id="cbc3f-106">O cmdlet **Get-AzHDInsightCluster** lista os clusters de serviço HDInsight do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="cbc3f-107">Use o *parâmetro ClusterName* para obter detalhes de um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="cbc3f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbc3f-108">EXAMPLES</span></span>

### <span data-ttu-id="cbc3f-109">Exemplo 1: Listar todos os clusters HDInsight do Azure</span><span class="sxs-lookup"><span data-stu-id="cbc3f-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="cbc3f-110">Este comando lista todos os clusters HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="cbc3f-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cbc3f-111">PARAMETERS</span></span>

### <span data-ttu-id="cbc3f-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cbc3f-112">-ClusterName</span></span>
<span data-ttu-id="cbc3f-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cbc3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc3f-114">-DefaultProfile</span></span>
<span data-ttu-id="cbc3f-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cbc3f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbc3f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbc3f-116">-ResourceGroupName</span></span>
<span data-ttu-id="cbc3f-117">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cbc3f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc3f-118">CommonParameters</span></span>
<span data-ttu-id="cbc3f-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbc3f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc3f-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbc3f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc3f-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbc3f-121">INPUTS</span></span>

### <span data-ttu-id="cbc3f-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cbc3f-122">None</span></span>

## <span data-ttu-id="cbc3f-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cbc3f-123">OUTPUTS</span></span>

### <span data-ttu-id="cbc3f-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cbc3f-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="cbc3f-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="cbc3f-125">NOTES</span></span>

## <span data-ttu-id="cbc3f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbc3f-126">RELATED LINKS</span></span>

[<span data-ttu-id="cbc3f-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cbc3f-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="cbc3f-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cbc3f-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


