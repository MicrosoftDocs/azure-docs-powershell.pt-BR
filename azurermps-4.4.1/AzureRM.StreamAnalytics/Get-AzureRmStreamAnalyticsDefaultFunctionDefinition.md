---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 307a07254f61bcbd37127a2a4d15bb41944a3508
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429941"
---
# <span data-ttu-id="41842-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="41842-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="41842-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41842-102">SYNOPSIS</span></span>
<span data-ttu-id="41842-103">Obtém a definição padrão de uma função no Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="41842-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41842-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41842-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41842-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41842-105">DESCRIPTION</span></span>
<span data-ttu-id="41842-106">O cmdlet **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** Obtém a definição padrão de uma função no Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="41842-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="41842-107">Você pode usar a definição padrão e o cmdlet New-AzureRmStreamAnalyticsFunction para criar uma função.</span><span class="sxs-lookup"><span data-stu-id="41842-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="41842-108">Você pode modificar a definição padrão antes de criar uma função.</span><span class="sxs-lookup"><span data-stu-id="41842-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="41842-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41842-109">EXAMPLES</span></span>

### <span data-ttu-id="41842-110">Exemplo 1: obter a definição padrão de uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="41842-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="41842-111">Esse comando obtém a definição padrão da função chamada ScoreTweet usando os parâmetros especificados no RetrieveDefaultDefinitionRequest.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="41842-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="41842-112">OS</span><span class="sxs-lookup"><span data-stu-id="41842-112">PARAMETERS</span></span>

### <span data-ttu-id="41842-113">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="41842-113">-File</span></span>
<span data-ttu-id="41842-114">Especifica o caminho de um arquivo. JSON que contém a representação JSON (JavaScript Object Notation) do corpo da solicitação da solicitação de definição da função padrão de recuperação.</span><span class="sxs-lookup"><span data-stu-id="41842-114">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="41842-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="41842-115">-JobName</span></span>
<span data-ttu-id="41842-116">Especifica o nome do trabalho do Stream Analytics ao qual as funções pertencem.</span><span class="sxs-lookup"><span data-stu-id="41842-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="41842-117">Esse cmdlet obtém a definição padrão para uma função no trabalho que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41842-117">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="41842-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="41842-118">-Name</span></span>
<span data-ttu-id="41842-119">Especifica o nome da função Stream Analytics para a qual esse cmdlet obtém a definição padrão.</span><span class="sxs-lookup"><span data-stu-id="41842-119">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="41842-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41842-120">-ResourceGroupName</span></span>
<span data-ttu-id="41842-121">Especifica o nome do grupo de recursos ao qual a função do Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="41842-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="41842-122">Esse cmdlet obtém uma definição de função para o grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41842-122">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="41842-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41842-123">-DefaultProfile</span></span>
<span data-ttu-id="41842-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41842-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41842-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41842-125">CommonParameters</span></span>
<span data-ttu-id="41842-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41842-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41842-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41842-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41842-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41842-128">INPUTS</span></span>

## <span data-ttu-id="41842-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41842-129">OUTPUTS</span></span>

### <span data-ttu-id="41842-130">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="41842-130">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="41842-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41842-131">NOTES</span></span>

## <span data-ttu-id="41842-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41842-132">RELATED LINKS</span></span>

[<span data-ttu-id="41842-133">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="41842-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)


