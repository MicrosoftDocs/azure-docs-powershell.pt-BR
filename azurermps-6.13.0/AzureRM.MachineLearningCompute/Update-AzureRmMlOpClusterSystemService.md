---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/update-azurermmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: 042c857efde915847e8ad809e84c91ddaa103b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430193"
---
# <span data-ttu-id="c1470-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="c1470-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="c1470-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1470-102">SYNOPSIS</span></span>
<span data-ttu-id="c1470-103">Inicia uma atualização nos serviços do sistema do cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="c1470-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1470-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1470-104">SYNTAX</span></span>

### <span data-ttu-id="c1470-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1470-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1470-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="c1470-106">StartUpdateWithInputObject</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1470-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="c1470-107">StartUpdateWithResourceId</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1470-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1470-108">DESCRIPTION</span></span>
<span data-ttu-id="c1470-109">Os serviços do sistema podem ser atualizados independentemente do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="c1470-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="c1470-110">Para iniciar uma atualização nos serviços do sistema, use este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1470-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="c1470-111">Se nenhuma atualização estiver disponível, uma atualização ainda será iniciada e retornará com êxito.</span><span class="sxs-lookup"><span data-stu-id="c1470-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="c1470-112">Depois que a atualização terminar, ele relata quando começou, terminou e se foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c1470-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="c1470-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1470-113">EXAMPLES</span></span>

### <span data-ttu-id="c1470-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1470-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="c1470-115">Inicia uma atualização dos serviços do sistema no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="c1470-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="c1470-116">OS</span><span class="sxs-lookup"><span data-stu-id="c1470-116">PARAMETERS</span></span>

### <span data-ttu-id="c1470-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1470-117">-DefaultProfile</span></span>
<span data-ttu-id="c1470-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1470-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1470-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1470-119">-InputObject</span></span>
<span data-ttu-id="c1470-120">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="c1470-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1470-121">-Name</span></span>
<span data-ttu-id="c1470-122">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="c1470-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1470-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1470-124">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="c1470-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1470-125">-ResourceId</span></span>
<span data-ttu-id="c1470-126">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="c1470-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c1470-127">-Confirm</span></span>
<span data-ttu-id="c1470-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1470-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1470-129">-WhatIf</span></span>
<span data-ttu-id="c1470-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1470-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1470-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1470-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1470-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1470-132">CommonParameters</span></span>
<span data-ttu-id="c1470-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1470-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1470-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1470-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1470-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1470-135">INPUTS</span></span>

### <span data-ttu-id="c1470-136">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="c1470-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="c1470-137">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c1470-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c1470-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c1470-138">System.String</span></span>

## <span data-ttu-id="c1470-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1470-139">OUTPUTS</span></span>

### <span data-ttu-id="c1470-140">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="c1470-140">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="c1470-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1470-141">NOTES</span></span>

## <span data-ttu-id="c1470-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1470-142">RELATED LINKS</span></span>