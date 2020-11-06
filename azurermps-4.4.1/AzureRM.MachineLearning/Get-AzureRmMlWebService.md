---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441037"
---
# <span data-ttu-id="86803-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="86803-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="86803-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86803-102">SYNOPSIS</span></span>
<span data-ttu-id="86803-103">Recupera as informações resumidas para um ou mais serviços Web.</span><span class="sxs-lookup"><span data-stu-id="86803-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86803-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86803-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86803-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86803-105">DESCRIPTION</span></span>
<span data-ttu-id="86803-106">Recupera informações de definição de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="86803-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="86803-107">Dependendo dos canceladores passados, o cmdlet retorna a definição de um serviço Web específico, uma coleção de defintions para os serviços Web de um grupo de recursos especificado na assinatura atual ou uma coleção de defintions para os serviços Web na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="86803-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="86803-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86803-108">EXAMPLES</span></span>

### <span data-ttu-id="86803-109">--------------------------Exemplo 1: obter detalhes de um serviço Web específico--------------------------</span><span class="sxs-lookup"><span data-stu-id="86803-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="86803-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="86803-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="86803-111">--------------------------Exemplo 2: obter todos os recursos do serviço Web na assinatura atual--------------------------</span><span class="sxs-lookup"><span data-stu-id="86803-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="86803-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="86803-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="86803-113">--------------------------Exemplo 3: obter todos os serviços Web na assinatura atual e o grupo de recursos fornecido--------------------------</span><span class="sxs-lookup"><span data-stu-id="86803-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="86803-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="86803-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="86803-115">OS</span><span class="sxs-lookup"><span data-stu-id="86803-115">PARAMETERS</span></span>

### <span data-ttu-id="86803-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="86803-116">-Name</span></span>
<span data-ttu-id="86803-117">O nome do serviço Web para o qual os detalhes são recuperados.</span><span class="sxs-lookup"><span data-stu-id="86803-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="86803-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86803-118">-ResourceGroupName</span></span>
<span data-ttu-id="86803-119">O grupo de recursos a partir do qual os detalhes do serviço Web são recuperados.</span><span class="sxs-lookup"><span data-stu-id="86803-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="86803-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86803-120">-DefaultProfile</span></span>
<span data-ttu-id="86803-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86803-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86803-122">-Região</span><span class="sxs-lookup"><span data-stu-id="86803-122">-Region</span></span>
<span data-ttu-id="86803-123">O nome da região</span><span class="sxs-lookup"><span data-stu-id="86803-123">The name of region</span></span>

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

### <span data-ttu-id="86803-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86803-124">CommonParameters</span></span>
<span data-ttu-id="86803-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86803-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86803-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86803-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86803-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86803-127">INPUTS</span></span>

## <span data-ttu-id="86803-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86803-128">OUTPUTS</span></span>

### <span data-ttu-id="86803-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="86803-129">None</span></span>

## <span data-ttu-id="86803-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86803-130">NOTES</span></span>
<span data-ttu-id="86803-131">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="86803-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="86803-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86803-132">RELATED LINKS</span></span>

