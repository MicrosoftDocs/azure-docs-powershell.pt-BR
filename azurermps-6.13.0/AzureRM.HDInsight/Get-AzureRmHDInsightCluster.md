---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: f232d1df7bef3800fc54b2469a51f3f69c8d4fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430274"
---
# <span data-ttu-id="8899d-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8899d-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="8899d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8899d-102">SYNOPSIS</span></span>
<span data-ttu-id="8899d-103">Obtém e lista todos os clusters do Azure HDInsight associados à assinatura atual ou um grupo de recursos especificado ou recupera um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="8899d-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8899d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8899d-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8899d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8899d-105">DESCRIPTION</span></span>
<span data-ttu-id="8899d-106">O cmdlet **Get-AzureRmHDInsightCluster** lista os clusters de serviço do Azure HDInsight para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8899d-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="8899d-107">Use o parâmetro *ClusterName* para obter detalhes de um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="8899d-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="8899d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8899d-108">EXAMPLES</span></span>

### <span data-ttu-id="8899d-109">Exemplo 1: listar todos os clusters do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="8899d-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="8899d-110">Esse comando lista todos os clusters do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8899d-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="8899d-111">OS</span><span class="sxs-lookup"><span data-stu-id="8899d-111">PARAMETERS</span></span>

### <span data-ttu-id="8899d-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8899d-112">-ClusterName</span></span>
<span data-ttu-id="8899d-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="8899d-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8899d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8899d-114">-DefaultProfile</span></span>
<span data-ttu-id="8899d-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8899d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8899d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8899d-116">-ResourceGroupName</span></span>
<span data-ttu-id="8899d-117">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8899d-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8899d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8899d-118">CommonParameters</span></span>
<span data-ttu-id="8899d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8899d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8899d-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8899d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8899d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8899d-121">INPUTS</span></span>

### <span data-ttu-id="8899d-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8899d-122">None</span></span>

## <span data-ttu-id="8899d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8899d-123">OUTPUTS</span></span>

### <span data-ttu-id="8899d-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8899d-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="8899d-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8899d-125">NOTES</span></span>

## <span data-ttu-id="8899d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8899d-126">RELATED LINKS</span></span>

[<span data-ttu-id="8899d-127">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8899d-127">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="8899d-128">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8899d-128">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


