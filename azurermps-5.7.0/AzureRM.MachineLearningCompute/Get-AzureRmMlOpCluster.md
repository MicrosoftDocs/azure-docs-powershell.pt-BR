---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 0e9eecf16a26be5367df5d8ad8b45a40e0050da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602640"
---
# <span data-ttu-id="ceea3-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="ceea3-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="ceea3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ceea3-102">SYNOPSIS</span></span>
<span data-ttu-id="ceea3-103">Obtém um objeto de cluster operacional de operação.</span><span class="sxs-lookup"><span data-stu-id="ceea3-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ceea3-104">SYNTAX</span></span>

### <span data-ttu-id="ceea3-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="ceea3-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ceea3-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ceea3-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ceea3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ceea3-107">DESCRIPTION</span></span>
<span data-ttu-id="ceea3-108">Obtém um objeto de cluster operacional de operação por nome ou grupo de recursos ou por assinatura.</span><span class="sxs-lookup"><span data-stu-id="ceea3-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="ceea3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ceea3-109">EXAMPLES</span></span>

### <span data-ttu-id="ceea3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ceea3-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="ceea3-111">Obtém um cluster de operação específico por nome.</span><span class="sxs-lookup"><span data-stu-id="ceea3-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="ceea3-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ceea3-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="ceea3-113">Obtém todos os clusters de operação de funcionamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ceea3-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="ceea3-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ceea3-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="ceea3-115">Obtém todos os clusters de operação de funcionamento em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ceea3-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="ceea3-116">OS</span><span class="sxs-lookup"><span data-stu-id="ceea3-116">PARAMETERS</span></span>

### <span data-ttu-id="ceea3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceea3-117">-DefaultProfile</span></span>
<span data-ttu-id="ceea3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ceea3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceea3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ceea3-119">-Name</span></span>
<span data-ttu-id="ceea3-120">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ceea3-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceea3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceea3-121">-ResourceGroupName</span></span>
<span data-ttu-id="ceea3-122">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ceea3-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceea3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceea3-123">CommonParameters</span></span>
<span data-ttu-id="ceea3-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceea3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceea3-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceea3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceea3-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ceea3-126">INPUTS</span></span>

### <span data-ttu-id="ceea3-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ceea3-127">None</span></span>

## <span data-ttu-id="ceea3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ceea3-128">OUTPUTS</span></span>

### <span data-ttu-id="ceea3-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="ceea3-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="ceea3-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. Commands. MachineLearningCompute, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ceea3-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ceea3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ceea3-131">NOTES</span></span>

## <span data-ttu-id="ceea3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ceea3-132">RELATED LINKS</span></span>

