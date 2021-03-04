---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 46e9ae8f4b6b4bb954bca158adb82c0d821d67eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892489"
---
# <span data-ttu-id="7dbc4-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="7dbc4-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="7dbc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dbc4-102">SYNOPSIS</span></span>
<span data-ttu-id="7dbc4-103">Exclui um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-103">Deletes a web service.</span></span>

## <span data-ttu-id="7dbc4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7dbc4-104">SYNTAX</span></span>

### <span data-ttu-id="7dbc4-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7dbc4-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbc4-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7dbc4-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dbc4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7dbc4-107">DESCRIPTION</span></span>
<span data-ttu-id="7dbc4-108">Exclui um serviço Web do Azure Machine Learning referenciado por grupo de recursos e nome.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="7dbc4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7dbc4-109">EXAMPLES</span></span>

### <span data-ttu-id="7dbc4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7dbc4-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="7dbc4-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7dbc4-111">PARAMETERS</span></span>

### <span data-ttu-id="7dbc4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dbc4-112">-DefaultProfile</span></span>
<span data-ttu-id="7dbc4-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7dbc4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7dbc4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7dbc4-114">-Force</span></span>
<span data-ttu-id="7dbc4-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7dbc4-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="7dbc4-116">-MlWebService</span></span>
<span data-ttu-id="7dbc4-117">O serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="7dbc4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7dbc4-118">-Name</span></span>
<span data-ttu-id="7dbc4-119">O nome do serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="7dbc4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dbc4-120">-ResourceGroupName</span></span>
<span data-ttu-id="7dbc4-121">O grupo de recursos do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="7dbc4-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7dbc4-122">-Confirm</span></span>
<span data-ttu-id="7dbc4-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dbc4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dbc4-124">-WhatIf</span></span>
<span data-ttu-id="7dbc4-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dbc4-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dbc4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dbc4-127">CommonParameters</span></span>
<span data-ttu-id="7dbc4-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dbc4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dbc4-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dbc4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dbc4-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7dbc4-130">INPUTS</span></span>

### <span data-ttu-id="7dbc4-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="7dbc4-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7dbc4-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7dbc4-132">OUTPUTS</span></span>

### <span data-ttu-id="7dbc4-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="7dbc4-133">System.Void</span></span>

## <span data-ttu-id="7dbc4-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="7dbc4-134">NOTES</span></span>
<span data-ttu-id="7dbc4-135">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7dbc4-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7dbc4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dbc4-136">RELATED LINKS</span></span>
