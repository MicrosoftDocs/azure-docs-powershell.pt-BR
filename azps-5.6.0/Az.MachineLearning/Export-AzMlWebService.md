---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 0fad6a81f895643f8783ca8d179d68e31eed6da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888485"
---
# <span data-ttu-id="e9877-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="e9877-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="e9877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9877-102">SYNOPSIS</span></span>
<span data-ttu-id="e9877-103">Exporta o objeto de definição do serviço Web como uma cadeia de caracteres formatada JSON.</span><span class="sxs-lookup"><span data-stu-id="e9877-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="e9877-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e9877-104">SYNTAX</span></span>

### <span data-ttu-id="e9877-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="e9877-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9877-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="e9877-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9877-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e9877-107">DESCRIPTION</span></span>
<span data-ttu-id="e9877-108">Exporta o objeto de definição para o serviço Web especificado como uma cadeia de caracteres formatada JSON.</span><span class="sxs-lookup"><span data-stu-id="e9877-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="e9877-109">Você pode retornar a cadeia de caracteres imediatamente ou salvá-la em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e9877-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="e9877-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9877-110">EXAMPLES</span></span>

### <span data-ttu-id="e9877-111">Exemplo 1: Exportar como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="e9877-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="e9877-112">Exemplo 2: Exportar para arquivo</span><span class="sxs-lookup"><span data-stu-id="e9877-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="e9877-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e9877-113">PARAMETERS</span></span>

### <span data-ttu-id="e9877-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9877-114">-DefaultProfile</span></span>
<span data-ttu-id="e9877-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e9877-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9877-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e9877-116">-Force</span></span>
<span data-ttu-id="e9877-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e9877-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9877-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="e9877-118">-OutputFile</span></span>
<span data-ttu-id="e9877-119">O caminho do arquivo para a definição exportada.</span><span class="sxs-lookup"><span data-stu-id="e9877-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9877-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="e9877-120">-ToJsonString</span></span>
<span data-ttu-id="e9877-121">Especifica que a definição será exportada como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="e9877-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9877-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="e9877-122">-WebService</span></span>
<span data-ttu-id="e9877-123">O objeto de definição do serviço Web a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="e9877-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9877-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9877-124">-Confirm</span></span>
<span data-ttu-id="e9877-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9877-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9877-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9877-126">-WhatIf</span></span>
<span data-ttu-id="e9877-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9877-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9877-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9877-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9877-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9877-129">CommonParameters</span></span>
<span data-ttu-id="e9877-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9877-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9877-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9877-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9877-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9877-132">INPUTS</span></span>

### <span data-ttu-id="e9877-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="e9877-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e9877-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e9877-134">OUTPUTS</span></span>

### <span data-ttu-id="e9877-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e9877-135">System.String</span></span>

## <span data-ttu-id="e9877-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="e9877-136">NOTES</span></span>
<span data-ttu-id="e9877-137">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e9877-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e9877-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9877-138">RELATED LINKS</span></span>
