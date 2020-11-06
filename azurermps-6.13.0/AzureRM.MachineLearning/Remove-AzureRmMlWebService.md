---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: c1d6ae6c1396e23398bc1b52f4f32458999072a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430882"
---
# <span data-ttu-id="e3469-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="e3469-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="e3469-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3469-102">SYNOPSIS</span></span>
<span data-ttu-id="e3469-103">Exclui um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="e3469-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3469-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3469-104">SYNTAX</span></span>

### <span data-ttu-id="e3469-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e3469-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3469-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e3469-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3469-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3469-107">DESCRIPTION</span></span>
<span data-ttu-id="e3469-108">Exclui um serviço Web do Azure Machine Learning referenciado pelo nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3469-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="e3469-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3469-109">EXAMPLES</span></span>

### <span data-ttu-id="e3469-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3469-110">Example 1</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="e3469-111">OS</span><span class="sxs-lookup"><span data-stu-id="e3469-111">PARAMETERS</span></span>

### <span data-ttu-id="e3469-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3469-112">-DefaultProfile</span></span>
<span data-ttu-id="e3469-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e3469-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3469-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e3469-114">-Force</span></span>
<span data-ttu-id="e3469-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e3469-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3469-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="e3469-116">-MlWebService</span></span>
<span data-ttu-id="e3469-117">O serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e3469-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3469-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3469-118">-Name</span></span>
<span data-ttu-id="e3469-119">O nome do serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e3469-119">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3469-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3469-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3469-121">O grupo de recursos do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="e3469-121">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3469-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e3469-122">-Confirm</span></span>
<span data-ttu-id="e3469-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3469-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3469-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3469-124">-WhatIf</span></span>
<span data-ttu-id="e3469-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3469-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3469-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3469-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3469-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3469-127">CommonParameters</span></span>
<span data-ttu-id="e3469-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3469-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3469-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3469-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3469-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3469-130">INPUTS</span></span>

### <span data-ttu-id="e3469-131">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="e3469-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="e3469-132">Parâmetros: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e3469-132">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="e3469-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3469-133">OUTPUTS</span></span>

### <span data-ttu-id="e3469-134">System. void</span><span class="sxs-lookup"><span data-stu-id="e3469-134">System.Void</span></span>

## <span data-ttu-id="e3469-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3469-135">NOTES</span></span>
<span data-ttu-id="e3469-136">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e3469-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e3469-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3469-137">RELATED LINKS</span></span>