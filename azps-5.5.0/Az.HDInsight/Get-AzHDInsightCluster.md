---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113806"
---
# <span data-ttu-id="c2fc6-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c2fc6-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="c2fc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fc6-103">Obtém e lista todos os clusters HDInsight do Azure associados à assinatura atual ou a um grupo de recursos especificado, ou recupera um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="c2fc6-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="c2fc6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2fc6-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2fc6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="c2fc6-106">O **cmdlet Get-AzHDInsightCluster** lista os clusters de serviço HDInsight do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c2fc6-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="c2fc6-107">Use o *parâmetro ClusterName* para obter detalhes de um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="c2fc6-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="c2fc6-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c2fc6-108">EXAMPLES</span></span>

### <span data-ttu-id="c2fc6-109">Exemplo 1: Listar todos os clusters HDInsight do Azure</span><span class="sxs-lookup"><span data-stu-id="c2fc6-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="c2fc6-110">Esse comando lista todos os clusters HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2fc6-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="c2fc6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2fc6-111">PARAMETERS</span></span>

### <span data-ttu-id="c2fc6-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c2fc6-112">-ClusterName</span></span>
<span data-ttu-id="c2fc6-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="c2fc6-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c2fc6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fc6-114">-DefaultProfile</span></span>
<span data-ttu-id="c2fc6-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c2fc6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2fc6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2fc6-116">-ResourceGroupName</span></span>
<span data-ttu-id="c2fc6-117">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2fc6-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c2fc6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fc6-118">CommonParameters</span></span>
<span data-ttu-id="c2fc6-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fc6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fc6-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2fc6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fc6-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="c2fc6-121">INPUTS</span></span>

### <span data-ttu-id="c2fc6-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c2fc6-122">None</span></span>

## <span data-ttu-id="c2fc6-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="c2fc6-123">OUTPUTS</span></span>

### <span data-ttu-id="c2fc6-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c2fc6-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="c2fc6-125">Notas</span><span class="sxs-lookup"><span data-stu-id="c2fc6-125">NOTES</span></span>

## <span data-ttu-id="c2fc6-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2fc6-126">RELATED LINKS</span></span>

[<span data-ttu-id="c2fc6-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c2fc6-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="c2fc6-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c2fc6-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


