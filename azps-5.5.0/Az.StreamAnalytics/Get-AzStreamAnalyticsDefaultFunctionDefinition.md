---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112480"
---
# <span data-ttu-id="ceae2-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="ceae2-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="ceae2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ceae2-102">SYNOPSIS</span></span>
<span data-ttu-id="ceae2-103">Obtém a definição padrão de uma função no Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ceae2-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="ceae2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ceae2-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceae2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ceae2-105">DESCRIPTION</span></span>
<span data-ttu-id="ceae2-106">O cmdlet **Get-AzStreamAnalyticsDefaultFunctionDefinition obtém** a definição padrão de uma função no Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ceae2-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="ceae2-107">Você pode usar a definição padrão e New-AzStreamAnalyticsFunction cmdlet para criar uma função.</span><span class="sxs-lookup"><span data-stu-id="ceae2-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="ceae2-108">Você pode modificar a definição padrão antes de criar uma função.</span><span class="sxs-lookup"><span data-stu-id="ceae2-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="ceae2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ceae2-109">EXAMPLES</span></span>

### <span data-ttu-id="ceae2-110">Exemplo 1: Obter a definição padrão de uma função de Análise de Fluxo</span><span class="sxs-lookup"><span data-stu-id="ceae2-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="ceae2-111">Esse comando obtém a definição padrão da função chamada ScoreTweet usando os parâmetros especificados no RetrieveDefaultDefinitionRequest.jsno arquivo.</span><span class="sxs-lookup"><span data-stu-id="ceae2-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="ceae2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ceae2-112">PARAMETERS</span></span>

### <span data-ttu-id="ceae2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceae2-113">-DefaultProfile</span></span>
<span data-ttu-id="ceae2-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ceae2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceae2-115">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="ceae2-115">-File</span></span>
<span data-ttu-id="ceae2-116">Especifica o caminho de um arquivo .json que contém a representação de JSON (Notação de Objeto JavaScript) do corpo da solicitação para a solicitação de definição de função padrão de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ceae2-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="ceae2-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="ceae2-117">-JobName</span></span>
<span data-ttu-id="ceae2-118">Especifica o nome do trabalho do Stream Analytics ao qual as funções pertencem.</span><span class="sxs-lookup"><span data-stu-id="ceae2-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="ceae2-119">Esse cmdlet obtém a definição padrão de uma função no trabalho especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ceae2-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="ceae2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ceae2-120">-Name</span></span>
<span data-ttu-id="ceae2-121">Especifica o nome da função Análise de Fluxo para a qual este cmdlet obtém a definição padrão.</span><span class="sxs-lookup"><span data-stu-id="ceae2-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceae2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceae2-122">-ResourceGroupName</span></span>
<span data-ttu-id="ceae2-123">Especifica o nome do grupo de recursos ao qual as funções do Stream Analytics pertencem.</span><span class="sxs-lookup"><span data-stu-id="ceae2-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="ceae2-124">Este cmdlet obtém uma definição de função para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ceae2-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ceae2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceae2-125">CommonParameters</span></span>
<span data-ttu-id="ceae2-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceae2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceae2-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceae2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceae2-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="ceae2-128">INPUTS</span></span>

### <span data-ttu-id="ceae2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ceae2-129">System.String</span></span>

## <span data-ttu-id="ceae2-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="ceae2-130">OUTPUTS</span></span>

### <span data-ttu-id="ceae2-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="ceae2-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="ceae2-132">Notas</span><span class="sxs-lookup"><span data-stu-id="ceae2-132">NOTES</span></span>

## <span data-ttu-id="ceae2-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ceae2-133">RELATED LINKS</span></span>

[<span data-ttu-id="ceae2-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="ceae2-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


