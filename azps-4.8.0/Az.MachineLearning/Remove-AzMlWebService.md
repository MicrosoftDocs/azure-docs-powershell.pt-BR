---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111667"
---
# <span data-ttu-id="277ee-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="277ee-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="277ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="277ee-102">SYNOPSIS</span></span>
<span data-ttu-id="277ee-103">Exclui um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="277ee-103">Deletes a web service.</span></span>

## <span data-ttu-id="277ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="277ee-104">SYNTAX</span></span>

### <span data-ttu-id="277ee-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="277ee-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="277ee-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="277ee-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="277ee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="277ee-107">DESCRIPTION</span></span>
<span data-ttu-id="277ee-108">Exclui um serviço Web do Azure Machine Learning referenciado pelo nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="277ee-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="277ee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="277ee-109">EXAMPLES</span></span>

### <span data-ttu-id="277ee-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="277ee-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="277ee-111">OS</span><span class="sxs-lookup"><span data-stu-id="277ee-111">PARAMETERS</span></span>

### <span data-ttu-id="277ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277ee-112">-DefaultProfile</span></span>
<span data-ttu-id="277ee-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="277ee-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="277ee-114">-Force</span><span class="sxs-lookup"><span data-stu-id="277ee-114">-Force</span></span>
<span data-ttu-id="277ee-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="277ee-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="277ee-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="277ee-116">-MlWebService</span></span>
<span data-ttu-id="277ee-117">O serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="277ee-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="277ee-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="277ee-118">-Name</span></span>
<span data-ttu-id="277ee-119">O nome do serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="277ee-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="277ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="277ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="277ee-121">O grupo de recursos do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="277ee-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="277ee-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="277ee-122">-Confirm</span></span>
<span data-ttu-id="277ee-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="277ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="277ee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277ee-124">-WhatIf</span></span>
<span data-ttu-id="277ee-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="277ee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="277ee-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="277ee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="277ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277ee-127">CommonParameters</span></span>
<span data-ttu-id="277ee-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="277ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277ee-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="277ee-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277ee-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="277ee-130">INPUTS</span></span>

### <span data-ttu-id="277ee-131">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="277ee-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="277ee-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="277ee-132">OUTPUTS</span></span>

### <span data-ttu-id="277ee-133">System. void</span><span class="sxs-lookup"><span data-stu-id="277ee-133">System.Void</span></span>

## <span data-ttu-id="277ee-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="277ee-134">NOTES</span></span>
<span data-ttu-id="277ee-135">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="277ee-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="277ee-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="277ee-136">RELATED LINKS</span></span>
