---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770439"
---
# <span data-ttu-id="db603-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="db603-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="db603-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db603-102">SYNOPSIS</span></span>
<span data-ttu-id="db603-103">Obtém um objeto de cluster operacional de operação.</span><span class="sxs-lookup"><span data-stu-id="db603-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="db603-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db603-104">SYNTAX</span></span>

### <span data-ttu-id="db603-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="db603-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db603-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db603-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db603-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db603-107">DESCRIPTION</span></span>
<span data-ttu-id="db603-108">Obtém um objeto de cluster operacional de operação por nome ou grupo de recursos ou por assinatura.</span><span class="sxs-lookup"><span data-stu-id="db603-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="db603-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db603-109">EXAMPLES</span></span>

### <span data-ttu-id="db603-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db603-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="db603-111">Obtém um cluster de operação específico por nome.</span><span class="sxs-lookup"><span data-stu-id="db603-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="db603-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="db603-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="db603-113">Obtém todos os clusters de operação de funcionamento em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db603-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="db603-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="db603-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="db603-115">Obtém todos os clusters de operação de funcionamento em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="db603-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="db603-116">OS</span><span class="sxs-lookup"><span data-stu-id="db603-116">PARAMETERS</span></span>

### <span data-ttu-id="db603-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db603-117">-DefaultProfile</span></span>
<span data-ttu-id="db603-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db603-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db603-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="db603-119">-Name</span></span>
<span data-ttu-id="db603-120">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="db603-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db603-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db603-121">-ResourceGroupName</span></span>
<span data-ttu-id="db603-122">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="db603-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db603-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db603-123">CommonParameters</span></span>
<span data-ttu-id="db603-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db603-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db603-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db603-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db603-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db603-126">INPUTS</span></span>

### <span data-ttu-id="db603-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="db603-127">None</span></span>

## <span data-ttu-id="db603-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db603-128">OUTPUTS</span></span>

### <span data-ttu-id="db603-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="db603-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="db603-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db603-130">NOTES</span></span>

## <span data-ttu-id="db603-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db603-131">RELATED LINKS</span></span>
