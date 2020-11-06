---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 0351a7b139b8bf68f8d7154b65949c1cdda4bbdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431537"
---
# <span data-ttu-id="a6239-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a6239-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="a6239-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6239-102">SYNOPSIS</span></span>
<span data-ttu-id="a6239-103">Cria ou substitui uma função em um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6239-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6239-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6239-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6239-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6239-105">DESCRIPTION</span></span>
<span data-ttu-id="a6239-106">O cmdlet **New-AzureRmStreamAnalyticsFunction** cria uma função em um trabalho do Stream Analytics do Azure ou substitui uma função existente.</span><span class="sxs-lookup"><span data-stu-id="a6239-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="a6239-107">Defina a função em um arquivo JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="a6239-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="a6239-108">Você pode especificar o nome da função usando o parâmetro *Name* ou o arquivo. JSON.</span><span class="sxs-lookup"><span data-stu-id="a6239-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="a6239-109">Se você especificar o nome de ambas as formas, os nomes deverão coincidir.</span><span class="sxs-lookup"><span data-stu-id="a6239-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="a6239-110">Para substituir uma função existente, especifique o nome da função existente.</span><span class="sxs-lookup"><span data-stu-id="a6239-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="a6239-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6239-111">EXAMPLES</span></span>

### <span data-ttu-id="a6239-112">Exemplo 1: criar uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="a6239-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="a6239-113">Esse comando cria uma função a partir do arquivo Function07.js.</span><span class="sxs-lookup"><span data-stu-id="a6239-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="a6239-114">O nome da função é armazenado no arquivo. JSON.</span><span class="sxs-lookup"><span data-stu-id="a6239-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="a6239-115">Exemplo 2: criar uma função do Stream Analytics chamada ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="a6239-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="a6239-116">Esse comando cria uma função no trabalho chamado ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="a6239-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="a6239-117">Exemplo 3: substituir uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="a6239-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="a6239-118">Esse comando substitui a definição da função existente chamada ScoreTweet pela definição em Function22.js.</span><span class="sxs-lookup"><span data-stu-id="a6239-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="a6239-119">OS</span><span class="sxs-lookup"><span data-stu-id="a6239-119">PARAMETERS</span></span>

### <span data-ttu-id="a6239-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6239-120">-DefaultProfile</span></span>
<span data-ttu-id="a6239-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6239-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6239-122">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="a6239-122">-File</span></span>
<span data-ttu-id="a6239-123">Especifica o caminho de um arquivo. JSON que contém a representação JSON da função Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6239-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6239-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a6239-124">-Force</span></span>
<span data-ttu-id="a6239-125">Indica que esse cmdlet substitui uma função de análise de fluxo existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="a6239-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6239-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="a6239-126">-JobName</span></span>
<span data-ttu-id="a6239-127">Especifica o nome do trabalho do Stream Analytics em que esse cmdlet cria uma função Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6239-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6239-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6239-128">-Name</span></span>
<span data-ttu-id="a6239-129">Especifica o nome da função do Stream Analytics que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="a6239-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6239-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6239-130">-ResourceGroupName</span></span>
<span data-ttu-id="a6239-131">Especifica o nome do grupo de recursos sob o qual esse cmdlet cria uma função Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6239-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6239-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6239-132">-Confirm</span></span>
<span data-ttu-id="a6239-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6239-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6239-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6239-134">-WhatIf</span></span>
<span data-ttu-id="a6239-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6239-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6239-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6239-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6239-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6239-137">CommonParameters</span></span>
<span data-ttu-id="a6239-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6239-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6239-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6239-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6239-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6239-140">INPUTS</span></span>

### <span data-ttu-id="a6239-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a6239-141">None</span></span>
<span data-ttu-id="a6239-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a6239-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6239-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6239-143">OUTPUTS</span></span>

### <span data-ttu-id="a6239-144">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="a6239-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="a6239-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6239-145">NOTES</span></span>

## <span data-ttu-id="a6239-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6239-146">RELATED LINKS</span></span>

[<span data-ttu-id="a6239-147">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a6239-147">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="a6239-148">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a6239-148">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="a6239-149">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a6239-149">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


