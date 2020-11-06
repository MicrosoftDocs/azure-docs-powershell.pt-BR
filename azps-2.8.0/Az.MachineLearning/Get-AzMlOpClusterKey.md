---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595979"
---
# <span data-ttu-id="ddaf0-101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="ddaf0-101">Get-AzMlOpClusterKey</span></span>

## <span data-ttu-id="ddaf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ddaf0-102">SYNOPSIS</span></span>
<span data-ttu-id="ddaf0-103">Obtém as teclas de acesso associadas a um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-103">Gets the access keys associated with an operationalization cluster.</span></span>

## <span data-ttu-id="ddaf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddaf0-104">SYNTAX</span></span>

### <span data-ttu-id="ddaf0-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddaf0-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddaf0-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="ddaf0-106">GetByInputObject</span></span>
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddaf0-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ddaf0-107">GetByResourceId</span></span>
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddaf0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ddaf0-108">DESCRIPTION</span></span>
<span data-ttu-id="ddaf0-109">As chaves para a conta de armazenamento, o registro de contêiner e outros serviços associados ao cluster de operação de funcionamento não são retornadas ao obter as propriedades do cluster.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="ddaf0-110">Uma chamada específica para recuperar as chaves deve ser feita, já que elas são informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="ddaf0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddaf0-111">EXAMPLES</span></span>

### <span data-ttu-id="ddaf0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ddaf0-112">Example 1</span></span>
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="ddaf0-113">Retorna as chaves secretas dos serviços associados ao cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="ddaf0-114">OS</span><span class="sxs-lookup"><span data-stu-id="ddaf0-114">PARAMETERS</span></span>

### <span data-ttu-id="ddaf0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddaf0-115">-DefaultProfile</span></span>
<span data-ttu-id="ddaf0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddaf0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddaf0-117">-InputObject</span></span>
<span data-ttu-id="ddaf0-118">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-118">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddaf0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddaf0-119">-Name</span></span>
<span data-ttu-id="ddaf0-120">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddaf0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddaf0-121">-ResourceGroupName</span></span>
<span data-ttu-id="ddaf0-122">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddaf0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddaf0-123">-ResourceId</span></span>
<span data-ttu-id="ddaf0-124">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddaf0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddaf0-125">CommonParameters</span></span>
<span data-ttu-id="ddaf0-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddaf0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddaf0-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddaf0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddaf0-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ddaf0-128">INPUTS</span></span>

### <span data-ttu-id="ddaf0-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="ddaf0-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="ddaf0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ddaf0-130">System.String</span></span>

## <span data-ttu-id="ddaf0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ddaf0-131">OUTPUTS</span></span>

### <span data-ttu-id="ddaf0-132">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="ddaf0-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="ddaf0-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ddaf0-133">NOTES</span></span>

## <span data-ttu-id="ddaf0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddaf0-134">RELATED LINKS</span></span>
