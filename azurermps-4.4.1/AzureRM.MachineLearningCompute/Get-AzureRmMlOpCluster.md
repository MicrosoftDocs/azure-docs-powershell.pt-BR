---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432615"
---
# <span data-ttu-id="75047-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="75047-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="75047-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75047-102">SYNOPSIS</span></span>
<span data-ttu-id="75047-103">Obtém um objeto de cluster operacional de operação.</span><span class="sxs-lookup"><span data-stu-id="75047-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75047-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75047-104">SYNTAX</span></span>

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75047-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75047-105">DESCRIPTION</span></span>
<span data-ttu-id="75047-106">Obtém um objeto de cluster operacional de operação por nome ou grupo de recursos ou por assinatura.</span><span class="sxs-lookup"><span data-stu-id="75047-106">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="75047-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75047-107">EXAMPLES</span></span>

### <span data-ttu-id="75047-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75047-108">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="75047-109">Obtém um cluster de operação específico por nome.</span><span class="sxs-lookup"><span data-stu-id="75047-109">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="75047-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="75047-110">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="75047-111">Obtém todos os clusters de operação de funcionamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75047-111">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="75047-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="75047-112">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="75047-113">Obtém todos os clusters de operação de funcionamento em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="75047-113">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="75047-114">OS</span><span class="sxs-lookup"><span data-stu-id="75047-114">PARAMETERS</span></span>

### <span data-ttu-id="75047-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75047-115">-DefaultProfile</span></span>
<span data-ttu-id="75047-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75047-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75047-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="75047-117">-Name</span></span>
<span data-ttu-id="75047-118">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="75047-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75047-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75047-119">-ResourceGroupName</span></span>
<span data-ttu-id="75047-120">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="75047-120">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="75047-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75047-121">CommonParameters</span></span>
<span data-ttu-id="75047-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75047-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75047-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75047-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75047-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75047-124">INPUTS</span></span>

### <span data-ttu-id="75047-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="75047-125">None</span></span>

## <span data-ttu-id="75047-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75047-126">OUTPUTS</span></span>

### <span data-ttu-id="75047-127">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="75047-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="75047-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="75047-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="75047-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75047-129">NOTES</span></span>

## <span data-ttu-id="75047-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75047-130">RELATED LINKS</span></span>

