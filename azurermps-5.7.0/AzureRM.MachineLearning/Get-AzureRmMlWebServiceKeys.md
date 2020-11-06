---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431005"
---
# <span data-ttu-id="1bdbc-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="1bdbc-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="1bdbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bdbc-102">SYNOPSIS</span></span>
<span data-ttu-id="1bdbc-103">Recupera as chaves do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="1bdbc-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bdbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bdbc-104">SYNTAX</span></span>

### <span data-ttu-id="1bdbc-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1bdbc-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bdbc-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="1bdbc-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bdbc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bdbc-107">DESCRIPTION</span></span>
<span data-ttu-id="1bdbc-108">Obtém as teclas de acesso para as APIs de tempo de execução do serviço Web do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="1bdbc-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="1bdbc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bdbc-109">EXAMPLES</span></span>

### <span data-ttu-id="1bdbc-110">--------------------------Exemplo 1-obter as chaves para um serviço Web especificado pelo nome e grupo de recursos--------------------------</span><span class="sxs-lookup"><span data-stu-id="1bdbc-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="1bdbc-111">--------------------------Exemplo 2-obter chaves para a instância do serviço Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="1bdbc-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="1bdbc-112">$mlService é um objeto do tipo Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="1bdbc-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="1bdbc-113">OS</span><span class="sxs-lookup"><span data-stu-id="1bdbc-113">PARAMETERS</span></span>

### <span data-ttu-id="1bdbc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bdbc-114">-DefaultProfile</span></span>
<span data-ttu-id="1bdbc-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1bdbc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bdbc-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="1bdbc-116">-MlWebService</span></span>
<span data-ttu-id="1bdbc-117">O nome do serviço Web para o qual as teclas de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="1bdbc-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bdbc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bdbc-118">-Name</span></span>
<span data-ttu-id="1bdbc-119">O nome do serviço Web para o qual as teclas de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="1bdbc-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bdbc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bdbc-120">-ResourceGroupName</span></span>
<span data-ttu-id="1bdbc-121">O grupo de recursos para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="1bdbc-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bdbc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bdbc-122">CommonParameters</span></span>
<span data-ttu-id="1bdbc-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bdbc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bdbc-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bdbc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bdbc-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bdbc-125">INPUTS</span></span>

### <span data-ttu-id="1bdbc-126">Serviço</span><span class="sxs-lookup"><span data-stu-id="1bdbc-126">WebService</span></span>
<span data-ttu-id="1bdbc-127">O parâmetro ' MlWebService ' aceita o valor do tipo ' WebService ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1bdbc-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="1bdbc-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bdbc-128">OUTPUTS</span></span>

### <span data-ttu-id="1bdbc-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1bdbc-129">None</span></span>

## <span data-ttu-id="1bdbc-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bdbc-130">NOTES</span></span>
<span data-ttu-id="1bdbc-131">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="1bdbc-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1bdbc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bdbc-132">RELATED LINKS</span></span>

