---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9f531b67d2dc3cc6010a7677c96dc4ecf10fb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430449"
---
# <span data-ttu-id="b7e35-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="b7e35-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="b7e35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7e35-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e35-103">Verifica se há atualizações disponíveis para os serviços do sistema associados a um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="b7e35-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7e35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7e35-104">SYNTAX</span></span>

### <span data-ttu-id="b7e35-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b7e35-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7e35-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7e35-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7e35-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7e35-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7e35-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7e35-108">DESCRIPTION</span></span>
<span data-ttu-id="b7e35-109">Os serviços do sistema recebem atualizações independentemente do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="b7e35-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="b7e35-110">Usar esse cmdlet permitirá que o usuário saiba se Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="b7e35-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="b7e35-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7e35-111">EXAMPLES</span></span>

### <span data-ttu-id="b7e35-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7e35-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="b7e35-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b7e35-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="b7e35-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b7e35-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="b7e35-115">OS</span><span class="sxs-lookup"><span data-stu-id="b7e35-115">PARAMETERS</span></span>

### <span data-ttu-id="b7e35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e35-116">-DefaultProfile</span></span>
<span data-ttu-id="b7e35-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7e35-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7e35-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7e35-118">-InputObject</span></span>
<span data-ttu-id="b7e35-119">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="b7e35-119">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e35-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7e35-120">-Name</span></span>
<span data-ttu-id="b7e35-121">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="b7e35-121">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e35-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e35-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7e35-123">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="b7e35-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e35-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7e35-124">-ResourceId</span></span>
<span data-ttu-id="b7e35-125">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="b7e35-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e35-126">CommonParameters</span></span>
<span data-ttu-id="b7e35-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e35-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e35-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e35-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7e35-129">INPUTS</span></span>

### <span data-ttu-id="b7e35-130">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="b7e35-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="b7e35-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b7e35-131">System.String</span></span>

## <span data-ttu-id="b7e35-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7e35-132">OUTPUTS</span></span>

### <span data-ttu-id="b7e35-133">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="b7e35-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="b7e35-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7e35-134">NOTES</span></span>

## <span data-ttu-id="b7e35-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7e35-135">RELATED LINKS</span></span>

