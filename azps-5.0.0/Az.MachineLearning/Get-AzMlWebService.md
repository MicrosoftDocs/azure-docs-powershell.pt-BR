---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126052"
---
# <span data-ttu-id="4f3bb-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="4f3bb-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="4f3bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3bb-103">Recupera as informações resumidas para um ou mais serviços Web.</span><span class="sxs-lookup"><span data-stu-id="4f3bb-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="4f3bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f3bb-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f3bb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f3bb-105">DESCRIPTION</span></span>
<span data-ttu-id="4f3bb-106">Recupera as informações de definição do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4f3bb-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="4f3bb-107">Dependendo dos parâmetros passados, o cmdlet retorna a definição de um serviço Web específico, um conjunto de definições dos serviços Web para um grupo de recursos especificado dentro da assinatura atual ou um conjunto de definições para os serviços Web na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4f3bb-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="4f3bb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f3bb-108">EXAMPLES</span></span>

### <span data-ttu-id="4f3bb-109">Exemplo 1: obter detalhes de um serviço Web específico</span><span class="sxs-lookup"><span data-stu-id="4f3bb-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="4f3bb-110">Exemplo 2: obter todos os recursos do serviço Web na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="4f3bb-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="4f3bb-111">Exemplo 3: obter todos os serviços Web na assinatura atual e o grupo de recursos fornecido</span><span class="sxs-lookup"><span data-stu-id="4f3bb-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="4f3bb-112">OS</span><span class="sxs-lookup"><span data-stu-id="4f3bb-112">PARAMETERS</span></span>

### <span data-ttu-id="4f3bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f3bb-113">-DefaultProfile</span></span>
<span data-ttu-id="4f3bb-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4f3bb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f3bb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f3bb-115">-Name</span></span>
<span data-ttu-id="4f3bb-116">O nome do serviço Web para o qual os detalhes são recuperados.</span><span class="sxs-lookup"><span data-stu-id="4f3bb-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="4f3bb-117">-Região</span><span class="sxs-lookup"><span data-stu-id="4f3bb-117">-Region</span></span>
<span data-ttu-id="4f3bb-118">O nome da região</span><span class="sxs-lookup"><span data-stu-id="4f3bb-118">The name of region</span></span>

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

### <span data-ttu-id="4f3bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f3bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f3bb-120">O grupo de recursos a partir do qual os detalhes do serviço Web são recuperados.</span><span class="sxs-lookup"><span data-stu-id="4f3bb-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="4f3bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3bb-121">CommonParameters</span></span>
<span data-ttu-id="4f3bb-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f3bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3bb-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f3bb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3bb-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f3bb-124">INPUTS</span></span>

### <span data-ttu-id="4f3bb-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4f3bb-125">None</span></span>

## <span data-ttu-id="4f3bb-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f3bb-126">OUTPUTS</span></span>

### <span data-ttu-id="4f3bb-127">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="4f3bb-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="4f3bb-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f3bb-128">NOTES</span></span>
<span data-ttu-id="4f3bb-129">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="4f3bb-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4f3bb-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f3bb-130">RELATED LINKS</span></span>
