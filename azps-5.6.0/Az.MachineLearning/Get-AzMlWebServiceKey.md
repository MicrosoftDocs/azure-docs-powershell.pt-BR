---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: 05adf2476c922fdea17a69bd33f74570309349ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886621"
---
# <span data-ttu-id="756d3-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="756d3-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="756d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="756d3-102">SYNOPSIS</span></span>
<span data-ttu-id="756d3-103">Recupera as chaves do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="756d3-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="756d3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="756d3-104">SYNTAX</span></span>

### <span data-ttu-id="756d3-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="756d3-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="756d3-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="756d3-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="756d3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="756d3-107">DESCRIPTION</span></span>
<span data-ttu-id="756d3-108">Obtém as chaves de acesso para as APIs de tempo de execução do serviço Web do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="756d3-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="756d3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="756d3-109">EXAMPLES</span></span>

### <span data-ttu-id="756d3-110">Exemplo 1 - Obter as chaves de um serviço Web especificado por grupo de recursos e nome</span><span class="sxs-lookup"><span data-stu-id="756d3-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="756d3-111">Exemplo 2 - Obter chaves para a instância do serviço Web</span><span class="sxs-lookup"><span data-stu-id="756d3-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="756d3-112">$mlService é um objeto do tipo Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="756d3-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="756d3-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="756d3-113">PARAMETERS</span></span>

### <span data-ttu-id="756d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756d3-114">-DefaultProfile</span></span>
<span data-ttu-id="756d3-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="756d3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="756d3-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="756d3-116">-MlWebService</span></span>
<span data-ttu-id="756d3-117">O nome do serviço Web para o qual as chaves de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="756d3-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="756d3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="756d3-118">-Name</span></span>
<span data-ttu-id="756d3-119">O nome do serviço Web para o qual as chaves de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="756d3-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756d3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="756d3-120">-ResourceGroupName</span></span>
<span data-ttu-id="756d3-121">O grupo de recursos do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="756d3-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756d3-122">CommonParameters</span></span>
<span data-ttu-id="756d3-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="756d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756d3-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="756d3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756d3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="756d3-125">INPUTS</span></span>

### <span data-ttu-id="756d3-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="756d3-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="756d3-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="756d3-127">OUTPUTS</span></span>

### <span data-ttu-id="756d3-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="756d3-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="756d3-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="756d3-129">NOTES</span></span>
<span data-ttu-id="756d3-130">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="756d3-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="756d3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="756d3-131">RELATED LINKS</span></span>
