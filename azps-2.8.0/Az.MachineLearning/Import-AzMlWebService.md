---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 7c885da5423e765cca3d18ce18957c0e64bb2c36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595973"
---
# <span data-ttu-id="f55b5-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="f55b5-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="f55b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f55b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f55b5-103">Importa um objeto JSON para uma definição de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f55b5-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="f55b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f55b5-104">SYNTAX</span></span>

### <span data-ttu-id="f55b5-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="f55b5-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f55b5-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="f55b5-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f55b5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f55b5-107">DESCRIPTION</span></span>
<span data-ttu-id="f55b5-108">O cmdlet Import-AzMlWebService importa, especificado diretamente ou em um arquivo referenciado, e cria um objeto de definição de serviço Web que pode ser passado para o cmdlet New-AzMlWebService.</span><span class="sxs-lookup"><span data-stu-id="f55b5-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="f55b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f55b5-109">EXAMPLES</span></span>

### <span data-ttu-id="f55b5-110">Exemplo 1: importar da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="f55b5-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="f55b5-111">Exemplo 2: importar do caminho do arquivo</span><span class="sxs-lookup"><span data-stu-id="f55b5-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="f55b5-112">OS</span><span class="sxs-lookup"><span data-stu-id="f55b5-112">PARAMETERS</span></span>

### <span data-ttu-id="f55b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55b5-113">-DefaultProfile</span></span>
<span data-ttu-id="f55b5-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f55b5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f55b5-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f55b5-115">-InputFile</span></span>
<span data-ttu-id="f55b5-116">O caminho para o arquivo que contém a definição do serviço Web a ser importado.</span><span class="sxs-lookup"><span data-stu-id="f55b5-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55b5-117">-Jsonstring</span><span class="sxs-lookup"><span data-stu-id="f55b5-117">-JsonString</span></span>
<span data-ttu-id="f55b5-118">A cadeia de caracteres formatada JSON que contém a definição do serviço Web a ser importada.</span><span class="sxs-lookup"><span data-stu-id="f55b5-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55b5-119">CommonParameters</span></span>
<span data-ttu-id="f55b5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55b5-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f55b5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55b5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f55b5-122">INPUTS</span></span>

### <span data-ttu-id="f55b5-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f55b5-123">None</span></span>

## <span data-ttu-id="f55b5-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f55b5-124">OUTPUTS</span></span>

### <span data-ttu-id="f55b5-125">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="f55b5-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f55b5-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f55b5-126">NOTES</span></span>
<span data-ttu-id="f55b5-127">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f55b5-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f55b5-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f55b5-128">RELATED LINKS</span></span>
