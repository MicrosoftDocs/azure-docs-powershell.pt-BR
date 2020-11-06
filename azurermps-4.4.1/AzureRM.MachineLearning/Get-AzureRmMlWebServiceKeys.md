---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441033"
---
# <span data-ttu-id="44e59-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="44e59-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="44e59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44e59-102">SYNOPSIS</span></span>
<span data-ttu-id="44e59-103">Recupera as chaves do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="44e59-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44e59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44e59-104">SYNTAX</span></span>

### <span data-ttu-id="44e59-105">Obtenha as chaves de acesso do serviço Web do Azure ML, de acordo com seu nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44e59-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44e59-106">Obtenha o KESY do Access para a instância do serviço Web especificada.</span><span class="sxs-lookup"><span data-stu-id="44e59-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44e59-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44e59-107">DESCRIPTION</span></span>
<span data-ttu-id="44e59-108">Obtém as teclas de acesso para as APIs de tempo de execução do serviço Web do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="44e59-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="44e59-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44e59-109">EXAMPLES</span></span>

### <span data-ttu-id="44e59-110">--------------------------Exemplo 1-obter as chaves para um serviço Web especificado pelo nome e grupo de recursos--------------------------</span><span class="sxs-lookup"><span data-stu-id="44e59-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="44e59-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="44e59-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="44e59-112">--------------------------Exemplo 2-obter chaves para a instância do serviço Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="44e59-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="44e59-113">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="44e59-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="44e59-114">$mlService é um objeto do tipo Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="44e59-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="44e59-115">OS</span><span class="sxs-lookup"><span data-stu-id="44e59-115">PARAMETERS</span></span>

### <span data-ttu-id="44e59-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="44e59-116">-MlWebService</span></span>
<span data-ttu-id="44e59-117">O nome do serviço Web para o qual as teclas de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="44e59-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44e59-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="44e59-118">-Name</span></span>
<span data-ttu-id="44e59-119">O nome do serviço Web para o qual as teclas de acesso são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="44e59-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e59-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44e59-120">-ResourceGroupName</span></span>
<span data-ttu-id="44e59-121">O grupo de recursos para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="44e59-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e59-122">-DefaultProfile</span></span>
<span data-ttu-id="44e59-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44e59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e59-124">CommonParameters</span></span>
<span data-ttu-id="44e59-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44e59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e59-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44e59-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e59-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44e59-127">INPUTS</span></span>

### <span data-ttu-id="44e59-128">Serviço</span><span class="sxs-lookup"><span data-stu-id="44e59-128">WebService</span></span>
<span data-ttu-id="44e59-129">O parâmetro ' MlWebService ' aceita o valor do tipo ' WebService ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="44e59-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="44e59-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44e59-130">OUTPUTS</span></span>

### <span data-ttu-id="44e59-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="44e59-131">None</span></span>

## <span data-ttu-id="44e59-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44e59-132">NOTES</span></span>
<span data-ttu-id="44e59-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="44e59-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="44e59-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44e59-134">RELATED LINKS</span></span>

