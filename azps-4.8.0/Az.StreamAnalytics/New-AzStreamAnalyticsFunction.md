---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 71a6267b06ce47ee36f220033ec598af3680deeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947487"
---
# <span data-ttu-id="35215-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="35215-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="35215-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35215-102">SYNOPSIS</span></span>
<span data-ttu-id="35215-103">Cria ou substitui uma função em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="35215-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="35215-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35215-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35215-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35215-105">DESCRIPTION</span></span>
<span data-ttu-id="35215-106">O cmdlet **New-AzStreamAnalyticsFunction** cria uma função em um trabalho do Stream Analytics do Azure ou substitui uma função existente.</span><span class="sxs-lookup"><span data-stu-id="35215-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="35215-107">Defina a função em um arquivo JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="35215-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="35215-108">Você pode especificar o nome da função usando o parâmetro *Name* ou o arquivo. JSON.</span><span class="sxs-lookup"><span data-stu-id="35215-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="35215-109">Se você especificar o nome de ambas as formas, os nomes deverão coincidir.</span><span class="sxs-lookup"><span data-stu-id="35215-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="35215-110">Para substituir uma função existente, especifique o nome da função existente.</span><span class="sxs-lookup"><span data-stu-id="35215-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="35215-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35215-111">EXAMPLES</span></span>

### <span data-ttu-id="35215-112">Exemplo 1: criar uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="35215-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="35215-113">Esse comando cria uma função a partir do arquivo Function07.js.</span><span class="sxs-lookup"><span data-stu-id="35215-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="35215-114">O nome da função é armazenado no arquivo. JSON.</span><span class="sxs-lookup"><span data-stu-id="35215-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="35215-115">Exemplo 2: criar uma função do Stream Analytics chamada ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="35215-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="35215-116">Esse comando cria uma função no trabalho chamado ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="35215-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="35215-117">Exemplo 3: substituir uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="35215-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="35215-118">Esse comando substitui a definição da função existente chamada ScoreTweet pela definição em Function22.js.</span><span class="sxs-lookup"><span data-stu-id="35215-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="35215-119">OS</span><span class="sxs-lookup"><span data-stu-id="35215-119">PARAMETERS</span></span>

### <span data-ttu-id="35215-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35215-120">-DefaultProfile</span></span>
<span data-ttu-id="35215-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35215-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35215-122">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="35215-122">-File</span></span>
<span data-ttu-id="35215-123">Especifica o caminho de um arquivo. JSON que contém a representação JSON da função Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="35215-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35215-124">-Force</span><span class="sxs-lookup"><span data-stu-id="35215-124">-Force</span></span>
<span data-ttu-id="35215-125">Indica que esse cmdlet substitui uma função de análise de fluxo existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="35215-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="35215-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="35215-126">-JobName</span></span>
<span data-ttu-id="35215-127">Especifica o nome do trabalho do Stream Analytics em que esse cmdlet cria uma função Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="35215-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35215-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="35215-128">-Name</span></span>
<span data-ttu-id="35215-129">Especifica o nome da função do Stream Analytics que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="35215-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35215-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35215-130">-ResourceGroupName</span></span>
<span data-ttu-id="35215-131">Especifica o nome do grupo de recursos sob o qual esse cmdlet cria uma função Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="35215-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35215-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35215-132">-Confirm</span></span>
<span data-ttu-id="35215-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35215-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35215-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35215-134">-WhatIf</span></span>
<span data-ttu-id="35215-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35215-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35215-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35215-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35215-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35215-137">CommonParameters</span></span>
<span data-ttu-id="35215-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35215-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35215-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35215-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35215-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35215-140">INPUTS</span></span>

### <span data-ttu-id="35215-141">System. String</span><span class="sxs-lookup"><span data-stu-id="35215-141">System.String</span></span>

## <span data-ttu-id="35215-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35215-142">OUTPUTS</span></span>

### <span data-ttu-id="35215-143">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="35215-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="35215-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35215-144">NOTES</span></span>

## <span data-ttu-id="35215-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35215-145">RELATED LINKS</span></span>

[<span data-ttu-id="35215-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="35215-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="35215-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="35215-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="35215-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="35215-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


