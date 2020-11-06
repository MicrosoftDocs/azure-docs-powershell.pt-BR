---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/update-azurermmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: 01f826746b92dd5aa82416e8207305b945ddb711
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603047"
---
# <span data-ttu-id="b38d4-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="b38d4-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="b38d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b38d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b38d4-103">Inicia uma atualização nos serviços do sistema do cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="b38d4-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b38d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b38d4-104">SYNTAX</span></span>

### <span data-ttu-id="b38d4-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b38d4-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b38d4-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="b38d4-106">StartUpdateWithInputObject</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b38d4-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="b38d4-107">StartUpdateWithResourceId</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b38d4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b38d4-108">DESCRIPTION</span></span>
<span data-ttu-id="b38d4-109">Os serviços do sistema podem ser atualizados independentemente do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="b38d4-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="b38d4-110">Para iniciar uma atualização nos serviços do sistema, use este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b38d4-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="b38d4-111">Se nenhuma atualização estiver disponível, uma atualização ainda será iniciada e retornará com êxito.</span><span class="sxs-lookup"><span data-stu-id="b38d4-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="b38d4-112">Depois que a atualização terminar, ele relata quando começou, terminou e se foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b38d4-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="b38d4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b38d4-113">EXAMPLES</span></span>

### <span data-ttu-id="b38d4-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b38d4-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="b38d4-115">Inicia uma atualização dos serviços do sistema no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="b38d4-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="b38d4-116">OS</span><span class="sxs-lookup"><span data-stu-id="b38d4-116">PARAMETERS</span></span>

### <span data-ttu-id="b38d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38d4-117">-DefaultProfile</span></span>
<span data-ttu-id="b38d4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b38d4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b38d4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b38d4-119">-InputObject</span></span>
<span data-ttu-id="b38d4-120">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="b38d4-120">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b38d4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b38d4-121">-Name</span></span>
<span data-ttu-id="b38d4-122">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="b38d4-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b38d4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b38d4-123">-ResourceGroupName</span></span>
<span data-ttu-id="b38d4-124">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="b38d4-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b38d4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b38d4-125">-ResourceId</span></span>
<span data-ttu-id="b38d4-126">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="b38d4-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b38d4-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b38d4-127">-Confirm</span></span>
<span data-ttu-id="b38d4-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b38d4-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b38d4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b38d4-129">-WhatIf</span></span>
<span data-ttu-id="b38d4-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b38d4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b38d4-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b38d4-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b38d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38d4-132">CommonParameters</span></span>
<span data-ttu-id="b38d4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b38d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38d4-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b38d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38d4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b38d4-135">INPUTS</span></span>

### <span data-ttu-id="b38d4-136">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="b38d4-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="b38d4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b38d4-137">System.String</span></span>

## <span data-ttu-id="b38d4-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b38d4-138">OUTPUTS</span></span>

### <span data-ttu-id="b38d4-139">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="b38d4-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="b38d4-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b38d4-140">NOTES</span></span>

## <span data-ttu-id="b38d4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b38d4-141">RELATED LINKS</span></span>

