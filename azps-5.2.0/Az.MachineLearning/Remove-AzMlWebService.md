---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260413"
---
# <span data-ttu-id="ed971-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="ed971-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="ed971-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed971-102">SYNOPSIS</span></span>
<span data-ttu-id="ed971-103">Exclui um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="ed971-103">Deletes a web service.</span></span>

## <span data-ttu-id="ed971-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed971-104">SYNTAX</span></span>

### <span data-ttu-id="ed971-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed971-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed971-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ed971-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed971-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed971-107">DESCRIPTION</span></span>
<span data-ttu-id="ed971-108">Exclui um serviço Web do Azure Machine Learning referenciado pelo nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed971-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="ed971-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed971-109">EXAMPLES</span></span>

### <span data-ttu-id="ed971-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed971-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="ed971-111">OS</span><span class="sxs-lookup"><span data-stu-id="ed971-111">PARAMETERS</span></span>

### <span data-ttu-id="ed971-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed971-112">-DefaultProfile</span></span>
<span data-ttu-id="ed971-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ed971-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed971-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ed971-114">-Force</span></span>
<span data-ttu-id="ed971-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="ed971-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ed971-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="ed971-116">-MlWebService</span></span>
<span data-ttu-id="ed971-117">O serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ed971-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="ed971-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed971-118">-Name</span></span>
<span data-ttu-id="ed971-119">O nome do serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ed971-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="ed971-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed971-120">-ResourceGroupName</span></span>
<span data-ttu-id="ed971-121">O grupo de recursos do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="ed971-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="ed971-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ed971-122">-Confirm</span></span>
<span data-ttu-id="ed971-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed971-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed971-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed971-124">-WhatIf</span></span>
<span data-ttu-id="ed971-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed971-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed971-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed971-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed971-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed971-127">CommonParameters</span></span>
<span data-ttu-id="ed971-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed971-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed971-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed971-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed971-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed971-130">INPUTS</span></span>

### <span data-ttu-id="ed971-131">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="ed971-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ed971-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed971-132">OUTPUTS</span></span>

### <span data-ttu-id="ed971-133">System. void</span><span class="sxs-lookup"><span data-stu-id="ed971-133">System.Void</span></span>

## <span data-ttu-id="ed971-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed971-134">NOTES</span></span>
<span data-ttu-id="ed971-135">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ed971-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ed971-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed971-136">RELATED LINKS</span></span>
