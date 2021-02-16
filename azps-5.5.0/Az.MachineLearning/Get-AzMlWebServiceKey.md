---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113598"
---
# <span data-ttu-id="7ba97-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="7ba97-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="7ba97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ba97-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba97-103">Recupera as chaves do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="7ba97-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="7ba97-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ba97-104">SYNTAX</span></span>

### <span data-ttu-id="7ba97-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7ba97-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ba97-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="7ba97-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ba97-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ba97-107">DESCRIPTION</span></span>
<span data-ttu-id="7ba97-108">Obtém as chaves de acesso para as APIs de tempo de execução do serviço Web do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="7ba97-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="7ba97-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ba97-109">EXAMPLES</span></span>

### <span data-ttu-id="7ba97-110">Exemplo 1 - Obter as chaves de um serviço Web especificado por nome e grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7ba97-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="7ba97-111">Exemplo 2 - Obter chaves para a instância do serviço Web</span><span class="sxs-lookup"><span data-stu-id="7ba97-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="7ba97-112">$mlService é um objeto do tipo Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="7ba97-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="7ba97-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ba97-113">PARAMETERS</span></span>

### <span data-ttu-id="7ba97-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba97-114">-DefaultProfile</span></span>
<span data-ttu-id="7ba97-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7ba97-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ba97-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="7ba97-116">-MlWebService</span></span>
<span data-ttu-id="7ba97-117">O nome do serviço Web para o qual as teclas de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7ba97-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="7ba97-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ba97-118">-Name</span></span>
<span data-ttu-id="7ba97-119">O nome do serviço Web para o qual as teclas de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7ba97-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="7ba97-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba97-120">-ResourceGroupName</span></span>
<span data-ttu-id="7ba97-121">O grupo de recursos do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="7ba97-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="7ba97-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba97-122">CommonParameters</span></span>
<span data-ttu-id="7ba97-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba97-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba97-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba97-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba97-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="7ba97-125">INPUTS</span></span>

### <span data-ttu-id="7ba97-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="7ba97-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7ba97-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="7ba97-127">OUTPUTS</span></span>

### <span data-ttu-id="7ba97-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="7ba97-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="7ba97-129">Notas</span><span class="sxs-lookup"><span data-stu-id="7ba97-129">NOTES</span></span>
<span data-ttu-id="7ba97-130">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7ba97-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7ba97-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ba97-131">RELATED LINKS</span></span>
