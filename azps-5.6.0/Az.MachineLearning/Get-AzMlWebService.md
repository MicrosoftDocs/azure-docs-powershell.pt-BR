---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: 1dcf881fbe0a3a616a7522236099f7698b50a1a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892624"
---
# <span data-ttu-id="fd068-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="fd068-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="fd068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd068-102">SYNOPSIS</span></span>
<span data-ttu-id="fd068-103">Recupera as informações de resumo de um ou mais serviços Web.</span><span class="sxs-lookup"><span data-stu-id="fd068-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="fd068-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fd068-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd068-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fd068-105">DESCRIPTION</span></span>
<span data-ttu-id="fd068-106">Recupera informações de definição de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="fd068-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="fd068-107">Dependendo dos parâmetros passados, o cmdlet retorna a definição de um serviço Web específico, uma coleção de definições para os serviços Web para um grupo de recursos especificado dentro da assinatura atual ou uma coleção de definições para os serviços Web dentro da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="fd068-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="fd068-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd068-108">EXAMPLES</span></span>

### <span data-ttu-id="fd068-109">Exemplo 1: Obter detalhes do serviço Web específico</span><span class="sxs-lookup"><span data-stu-id="fd068-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="fd068-110">Exemplo 2: Obter todos os recursos do serviço Web na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="fd068-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="fd068-111">Exemplo 3: Obter todos os serviços Web na assinatura atual e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fd068-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="fd068-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fd068-112">PARAMETERS</span></span>

### <span data-ttu-id="fd068-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd068-113">-DefaultProfile</span></span>
<span data-ttu-id="fd068-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fd068-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd068-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fd068-115">-Name</span></span>
<span data-ttu-id="fd068-116">O nome do serviço Web para o qual os detalhes são recuperados.</span><span class="sxs-lookup"><span data-stu-id="fd068-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd068-117">-Region</span><span class="sxs-lookup"><span data-stu-id="fd068-117">-Region</span></span>
<span data-ttu-id="fd068-118">O nome da região</span><span class="sxs-lookup"><span data-stu-id="fd068-118">The name of region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd068-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd068-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd068-120">O grupo de recursos do qual os detalhes do serviço Web são recuperados.</span><span class="sxs-lookup"><span data-stu-id="fd068-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd068-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd068-121">CommonParameters</span></span>
<span data-ttu-id="fd068-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd068-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd068-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd068-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd068-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd068-124">INPUTS</span></span>

### <span data-ttu-id="fd068-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fd068-125">None</span></span>

## <span data-ttu-id="fd068-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fd068-126">OUTPUTS</span></span>

### <span data-ttu-id="fd068-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="fd068-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="fd068-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="fd068-128">NOTES</span></span>
<span data-ttu-id="fd068-129">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="fd068-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fd068-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd068-130">RELATED LINKS</span></span>
