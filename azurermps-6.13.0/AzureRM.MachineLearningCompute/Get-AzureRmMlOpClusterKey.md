---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 6b5797d67b709e9c44756dad018a47eb416ed174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430198"
---
# <span data-ttu-id="cd468-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="cd468-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="cd468-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd468-102">SYNOPSIS</span></span>
<span data-ttu-id="cd468-103">Obtém as teclas de acesso associadas a um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="cd468-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd468-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd468-104">SYNTAX</span></span>

### <span data-ttu-id="cd468-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cd468-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd468-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd468-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd468-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd468-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd468-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd468-108">DESCRIPTION</span></span>
<span data-ttu-id="cd468-109">As chaves para a conta de armazenamento, o registro de contêiner e outros serviços associados ao cluster de operação de funcionamento não são retornadas ao obter as propriedades do cluster.</span><span class="sxs-lookup"><span data-stu-id="cd468-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="cd468-110">Uma chamada específica para recuperar as chaves deve ser feita, já que elas são informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="cd468-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="cd468-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd468-111">EXAMPLES</span></span>

### <span data-ttu-id="cd468-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd468-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="cd468-113">Retorna as chaves secretas dos serviços associados ao cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="cd468-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="cd468-114">OS</span><span class="sxs-lookup"><span data-stu-id="cd468-114">PARAMETERS</span></span>

### <span data-ttu-id="cd468-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd468-115">-DefaultProfile</span></span>
<span data-ttu-id="cd468-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd468-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd468-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd468-117">-InputObject</span></span>
<span data-ttu-id="cd468-118">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="cd468-118">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="cd468-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd468-119">-Name</span></span>
<span data-ttu-id="cd468-120">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="cd468-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="cd468-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd468-121">-ResourceGroupName</span></span>
<span data-ttu-id="cd468-122">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="cd468-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="cd468-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd468-123">-ResourceId</span></span>
<span data-ttu-id="cd468-124">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="cd468-124">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="cd468-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd468-125">CommonParameters</span></span>
<span data-ttu-id="cd468-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd468-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd468-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd468-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd468-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd468-128">INPUTS</span></span>

### <span data-ttu-id="cd468-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="cd468-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="cd468-130">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd468-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="cd468-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cd468-131">System.String</span></span>

## <span data-ttu-id="cd468-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd468-132">OUTPUTS</span></span>

### <span data-ttu-id="cd468-133">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="cd468-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="cd468-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd468-134">NOTES</span></span>

## <span data-ttu-id="cd468-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd468-135">RELATED LINKS</span></span>
