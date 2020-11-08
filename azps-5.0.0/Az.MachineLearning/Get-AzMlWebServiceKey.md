---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124878"
---
# <span data-ttu-id="86be4-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="86be4-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="86be4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86be4-102">SYNOPSIS</span></span>
<span data-ttu-id="86be4-103">Recupera as chaves do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="86be4-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="86be4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86be4-104">SYNTAX</span></span>

### <span data-ttu-id="86be4-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="86be4-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86be4-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="86be4-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86be4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86be4-107">DESCRIPTION</span></span>
<span data-ttu-id="86be4-108">Obtém as teclas de acesso para as APIs de tempo de execução do serviço Web do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="86be4-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="86be4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86be4-109">EXAMPLES</span></span>

### <span data-ttu-id="86be4-110">Exemplo 1-obter as chaves para um serviço Web especificado pelo grupo de recursos e nome</span><span class="sxs-lookup"><span data-stu-id="86be4-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="86be4-111">Exemplo 2-obter chaves para a instância do serviço Web</span><span class="sxs-lookup"><span data-stu-id="86be4-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="86be4-112">$mlService é um objeto do tipo Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="86be4-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="86be4-113">OS</span><span class="sxs-lookup"><span data-stu-id="86be4-113">PARAMETERS</span></span>

### <span data-ttu-id="86be4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86be4-114">-DefaultProfile</span></span>
<span data-ttu-id="86be4-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="86be4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86be4-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="86be4-116">-MlWebService</span></span>
<span data-ttu-id="86be4-117">O nome do serviço Web para o qual as teclas de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="86be4-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="86be4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="86be4-118">-Name</span></span>
<span data-ttu-id="86be4-119">O nome do serviço Web para o qual as teclas de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="86be4-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="86be4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86be4-120">-ResourceGroupName</span></span>
<span data-ttu-id="86be4-121">O grupo de recursos para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="86be4-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="86be4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86be4-122">CommonParameters</span></span>
<span data-ttu-id="86be4-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86be4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86be4-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86be4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86be4-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86be4-125">INPUTS</span></span>

### <span data-ttu-id="86be4-126">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="86be4-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="86be4-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86be4-127">OUTPUTS</span></span>

### <span data-ttu-id="86be4-128">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="86be4-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="86be4-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86be4-129">NOTES</span></span>
<span data-ttu-id="86be4-130">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="86be4-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="86be4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86be4-131">RELATED LINKS</span></span>
