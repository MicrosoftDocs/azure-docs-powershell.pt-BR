---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126059"
---
# <span data-ttu-id="38faf-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="38faf-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="38faf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38faf-102">SYNOPSIS</span></span>
<span data-ttu-id="38faf-103">Exporta o objeto de definição do serviço Web como uma cadeia de caracteres formatada como JSON.</span><span class="sxs-lookup"><span data-stu-id="38faf-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="38faf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38faf-104">SYNTAX</span></span>

### <span data-ttu-id="38faf-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="38faf-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38faf-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="38faf-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38faf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38faf-107">DESCRIPTION</span></span>
<span data-ttu-id="38faf-108">Exporta o objeto de definição para o serviço Web especificado como uma cadeia de caracteres formatada como JSON.</span><span class="sxs-lookup"><span data-stu-id="38faf-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="38faf-109">Você pode retornar a cadeia de caracteres imediatamente ou salvá-la em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="38faf-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="38faf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38faf-110">EXAMPLES</span></span>

### <span data-ttu-id="38faf-111">Exemplo 1: exportar como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="38faf-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="38faf-112">Exemplo 2: exportar para arquivo</span><span class="sxs-lookup"><span data-stu-id="38faf-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="38faf-113">OS</span><span class="sxs-lookup"><span data-stu-id="38faf-113">PARAMETERS</span></span>

### <span data-ttu-id="38faf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38faf-114">-DefaultProfile</span></span>
<span data-ttu-id="38faf-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="38faf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38faf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="38faf-116">-Force</span></span>
<span data-ttu-id="38faf-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="38faf-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="38faf-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="38faf-118">-OutputFile</span></span>
<span data-ttu-id="38faf-119">O caminho do arquivo para a definição exportada.</span><span class="sxs-lookup"><span data-stu-id="38faf-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="38faf-120">-ToJSONString</span><span class="sxs-lookup"><span data-stu-id="38faf-120">-ToJsonString</span></span>
<span data-ttu-id="38faf-121">Especifica que a definição será exportada como uma cadeia de caracteres JSON.</span><span class="sxs-lookup"><span data-stu-id="38faf-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="38faf-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="38faf-122">-WebService</span></span>
<span data-ttu-id="38faf-123">O objeto de definição de serviço Web a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="38faf-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="38faf-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38faf-124">-Confirm</span></span>
<span data-ttu-id="38faf-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38faf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38faf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38faf-126">-WhatIf</span></span>
<span data-ttu-id="38faf-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38faf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38faf-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38faf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38faf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38faf-129">CommonParameters</span></span>
<span data-ttu-id="38faf-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38faf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38faf-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38faf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38faf-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38faf-132">INPUTS</span></span>

### <span data-ttu-id="38faf-133">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="38faf-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="38faf-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38faf-134">OUTPUTS</span></span>

### <span data-ttu-id="38faf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="38faf-135">System.String</span></span>

## <span data-ttu-id="38faf-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38faf-136">NOTES</span></span>
<span data-ttu-id="38faf-137">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="38faf-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="38faf-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38faf-138">RELATED LINKS</span></span>
