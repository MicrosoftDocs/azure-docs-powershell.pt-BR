---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113594"
---
# <span data-ttu-id="3f935-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="3f935-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="3f935-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f935-102">SYNOPSIS</span></span>
<span data-ttu-id="3f935-103">Exclui um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="3f935-103">Deletes a web service.</span></span>

## <span data-ttu-id="3f935-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f935-104">SYNTAX</span></span>

### <span data-ttu-id="3f935-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3f935-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f935-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3f935-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f935-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f935-107">DESCRIPTION</span></span>
<span data-ttu-id="3f935-108">Exclui um serviço Web do Azure Machine Learning referenciado por nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f935-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="3f935-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f935-109">EXAMPLES</span></span>

### <span data-ttu-id="3f935-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f935-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="3f935-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f935-111">PARAMETERS</span></span>

### <span data-ttu-id="3f935-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f935-112">-DefaultProfile</span></span>
<span data-ttu-id="3f935-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3f935-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f935-114">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3f935-114">-Force</span></span>
<span data-ttu-id="3f935-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3f935-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3f935-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="3f935-116">-MlWebService</span></span>
<span data-ttu-id="3f935-117">O serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3f935-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="3f935-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f935-118">-Name</span></span>
<span data-ttu-id="3f935-119">O nome do serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="3f935-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="3f935-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f935-120">-ResourceGroupName</span></span>
<span data-ttu-id="3f935-121">O grupo de recursos do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="3f935-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="3f935-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3f935-122">-Confirm</span></span>
<span data-ttu-id="3f935-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f935-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f935-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f935-124">-WhatIf</span></span>
<span data-ttu-id="3f935-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3f935-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f935-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f935-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f935-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f935-127">CommonParameters</span></span>
<span data-ttu-id="3f935-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f935-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f935-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f935-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f935-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="3f935-130">INPUTS</span></span>

### <span data-ttu-id="3f935-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="3f935-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="3f935-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="3f935-132">OUTPUTS</span></span>

### <span data-ttu-id="3f935-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="3f935-133">System.Void</span></span>

## <span data-ttu-id="3f935-134">Notas</span><span class="sxs-lookup"><span data-stu-id="3f935-134">NOTES</span></span>
<span data-ttu-id="3f935-135">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3f935-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3f935-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f935-136">RELATED LINKS</span></span>
