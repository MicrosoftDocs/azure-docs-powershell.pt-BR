---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 02588ded441c1ac9f23deb19b763c099ce6c18ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770449"
---
# <span data-ttu-id="a4dc4-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="a4dc4-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="a4dc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dc4-103">Exporta o objeto de definição do serviço Web como uma cadeia de caracteres formatada como JSON.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="a4dc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4dc4-104">SYNTAX</span></span>

### <span data-ttu-id="a4dc4-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="a4dc4-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4dc4-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="a4dc4-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4dc4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4dc4-107">DESCRIPTION</span></span>
<span data-ttu-id="a4dc4-108">Exporta o objeto de definição para o serv. da Web especificado como uma cadeia de caracteres formatada como JSON.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="a4dc4-109">Você pode retornar a cadeia de caracteres imediatamente ou salvá-la em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="a4dc4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4dc4-110">EXAMPLES</span></span>

### <span data-ttu-id="a4dc4-111">Exemplo 1: exportar como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a4dc4-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="a4dc4-112">Exemplo 2: exportar para arquivo</span><span class="sxs-lookup"><span data-stu-id="a4dc4-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="a4dc4-113">OS</span><span class="sxs-lookup"><span data-stu-id="a4dc4-113">PARAMETERS</span></span>

### <span data-ttu-id="a4dc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dc4-114">-DefaultProfile</span></span>
<span data-ttu-id="a4dc4-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a4dc4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4dc4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a4dc4-116">-Force</span></span>
<span data-ttu-id="a4dc4-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a4dc4-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="a4dc4-118">-OutputFile</span></span>
<span data-ttu-id="a4dc4-119">O caminho do arquivo para a definição exportada.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="a4dc4-120">-ToJSONString</span><span class="sxs-lookup"><span data-stu-id="a4dc4-120">-ToJsonString</span></span>
<span data-ttu-id="a4dc4-121">Especifica que a definição será exportada como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="a4dc4-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="a4dc4-122">-WebService</span></span>
<span data-ttu-id="a4dc4-123">O objeto de definição de serviço Web a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="a4dc4-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a4dc4-124">-Confirm</span></span>
<span data-ttu-id="a4dc4-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4dc4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4dc4-126">-WhatIf</span></span>
<span data-ttu-id="a4dc4-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4dc4-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4dc4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dc4-129">CommonParameters</span></span>
<span data-ttu-id="a4dc4-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4dc4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dc4-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4dc4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dc4-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4dc4-132">INPUTS</span></span>

### <span data-ttu-id="a4dc4-133">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="a4dc4-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="a4dc4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4dc4-134">OUTPUTS</span></span>

### <span data-ttu-id="a4dc4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dc4-135">System.String</span></span>

## <span data-ttu-id="a4dc4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4dc4-136">NOTES</span></span>
<span data-ttu-id="a4dc4-137">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="a4dc4-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a4dc4-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4dc4-138">RELATED LINKS</span></span>
