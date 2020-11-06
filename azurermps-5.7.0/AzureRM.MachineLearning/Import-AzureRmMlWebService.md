---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: cc6c596b028ca7a4b89083ff06d37b3df9c3ed7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431004"
---
# <span data-ttu-id="77371-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="77371-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="77371-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77371-102">SYNOPSIS</span></span>
<span data-ttu-id="77371-103">Importa um objeto JSON para uma definição de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="77371-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77371-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77371-104">SYNTAX</span></span>

### <span data-ttu-id="77371-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="77371-105">ImportFromJSONFile</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77371-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="77371-106">ImportFromJSONString.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77371-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77371-107">DESCRIPTION</span></span>
<span data-ttu-id="77371-108">O cmdlet Import-AzureRmMlWebService importa, especificado diretamente ou em um arquivo referenciado, e cria um objeto de definição de serviço Web que pode ser passado para o cmdlet New-AzureRmMlWebService.</span><span class="sxs-lookup"><span data-stu-id="77371-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="77371-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77371-109">EXAMPLES</span></span>

### <span data-ttu-id="77371-110">--------------------------Exemplo 1: importar da cadeia de caracteres--------------------------</span><span class="sxs-lookup"><span data-stu-id="77371-110">--------------------------  Example 1: Import from string  --------------------------</span></span>
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="77371-111">--------------------------Exemplo 2: importar do caminho do arquivo--------------------------</span><span class="sxs-lookup"><span data-stu-id="77371-111">--------------------------  Example 2: Import from file path  --------------------------</span></span>
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="77371-112">OS</span><span class="sxs-lookup"><span data-stu-id="77371-112">PARAMETERS</span></span>

### <span data-ttu-id="77371-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77371-113">-DefaultProfile</span></span>
<span data-ttu-id="77371-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="77371-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77371-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="77371-115">-InputFile</span></span>
<span data-ttu-id="77371-116">O caminho para o arquivo que contém a definição do serviço Web a ser importado.</span><span class="sxs-lookup"><span data-stu-id="77371-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromJSONFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77371-117">-Jsonstring</span><span class="sxs-lookup"><span data-stu-id="77371-117">-JsonString</span></span>
<span data-ttu-id="77371-118">A cadeia de caracteres formatada JSON que contém a definição do serviço Web a ser importada.</span><span class="sxs-lookup"><span data-stu-id="77371-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromJSONString.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77371-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77371-119">CommonParameters</span></span>
<span data-ttu-id="77371-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77371-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77371-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77371-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77371-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77371-122">INPUTS</span></span>

### <span data-ttu-id="77371-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="77371-123">None</span></span>
<span data-ttu-id="77371-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="77371-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77371-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77371-125">OUTPUTS</span></span>

### <span data-ttu-id="77371-126">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="77371-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="77371-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77371-127">NOTES</span></span>
<span data-ttu-id="77371-128">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="77371-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="77371-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77371-129">RELATED LINKS</span></span>

