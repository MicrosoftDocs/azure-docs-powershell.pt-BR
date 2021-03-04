---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: e30ecc151da5e4a202b8da63f8d57a8f25c387dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886620"
---
# <span data-ttu-id="47e17-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="47e17-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="47e17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e17-102">SYNOPSIS</span></span>
<span data-ttu-id="47e17-103">Importa um objeto JSON para uma definição de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="47e17-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="47e17-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="47e17-104">SYNTAX</span></span>

### <span data-ttu-id="47e17-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="47e17-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47e17-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="47e17-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47e17-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="47e17-107">DESCRIPTION</span></span>
<span data-ttu-id="47e17-108">O Import-AzMlWebService cmdlet importa , especificado diretamente ou em um arquivo referenciado, e cria um objeto de definição de serviço Web que pode ser passado para o cmdlet New-AzMlWebService web.</span><span class="sxs-lookup"><span data-stu-id="47e17-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="47e17-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47e17-109">EXAMPLES</span></span>

### <span data-ttu-id="47e17-110">Exemplo 1: Importar da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="47e17-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="47e17-111">Exemplo 2: Importar do caminho do arquivo</span><span class="sxs-lookup"><span data-stu-id="47e17-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="47e17-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="47e17-112">PARAMETERS</span></span>

### <span data-ttu-id="47e17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e17-113">-DefaultProfile</span></span>
<span data-ttu-id="47e17-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="47e17-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47e17-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="47e17-115">-InputFile</span></span>
<span data-ttu-id="47e17-116">O caminho para o arquivo que contém a definição do serviço Web a ser importado.</span><span class="sxs-lookup"><span data-stu-id="47e17-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="47e17-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="47e17-117">-JsonString</span></span>
<span data-ttu-id="47e17-118">A cadeia de caracteres formatada JSON que contém a definição do serviço Web a ser importada.</span><span class="sxs-lookup"><span data-stu-id="47e17-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="47e17-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e17-119">CommonParameters</span></span>
<span data-ttu-id="47e17-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e17-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e17-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e17-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e17-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47e17-122">INPUTS</span></span>

### <span data-ttu-id="47e17-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="47e17-123">None</span></span>

## <span data-ttu-id="47e17-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="47e17-124">OUTPUTS</span></span>

### <span data-ttu-id="47e17-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="47e17-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="47e17-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="47e17-126">NOTES</span></span>
<span data-ttu-id="47e17-127">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="47e17-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="47e17-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47e17-128">RELATED LINKS</span></span>
