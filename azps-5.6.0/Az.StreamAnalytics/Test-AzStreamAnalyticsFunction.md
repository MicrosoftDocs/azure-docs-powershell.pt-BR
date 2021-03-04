---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d45a46cd0ff38f925a218c2bbab6edf70b97a4ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886823"
---
# <span data-ttu-id="f5d09-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f5d09-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="f5d09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5d09-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d09-103">Testa se o Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="f5d09-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="f5d09-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f5d09-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5d09-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f5d09-105">DESCRIPTION</span></span>
<span data-ttu-id="f5d09-106">O cmdlet **Test-AzStreamAnalyticsFunction** testa se o Azure Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="f5d09-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="f5d09-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5d09-107">EXAMPLES</span></span>

### <span data-ttu-id="f5d09-108">Exemplo 1: Testar uma função de Análise de Fluxo</span><span class="sxs-lookup"><span data-stu-id="f5d09-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="f5d09-109">Este comando testa o status de conexão da função denominada ScoreTweet no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="f5d09-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="f5d09-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f5d09-110">PARAMETERS</span></span>

### <span data-ttu-id="f5d09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d09-111">-DefaultProfile</span></span>
<span data-ttu-id="f5d09-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f5d09-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5d09-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="f5d09-113">-JobName</span></span>
<span data-ttu-id="f5d09-114">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="f5d09-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="f5d09-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f5d09-115">-Name</span></span>
<span data-ttu-id="f5d09-116">Especifica o nome da função Stream Analytics que este cmdlet testa.</span><span class="sxs-lookup"><span data-stu-id="f5d09-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="f5d09-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5d09-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5d09-118">Especifica o nome do grupo de recursos ao qual pertence uma função Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="f5d09-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="f5d09-119">Este cmdlet testa uma função no grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f5d09-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5d09-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d09-120">CommonParameters</span></span>
<span data-ttu-id="f5d09-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d09-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d09-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d09-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d09-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5d09-123">INPUTS</span></span>

### <span data-ttu-id="f5d09-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f5d09-124">System.String</span></span>

## <span data-ttu-id="f5d09-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f5d09-125">OUTPUTS</span></span>

### <span data-ttu-id="f5d09-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f5d09-126">System.Boolean</span></span>

## <span data-ttu-id="f5d09-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="f5d09-127">NOTES</span></span>

## <span data-ttu-id="f5d09-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5d09-128">RELATED LINKS</span></span>

[<span data-ttu-id="f5d09-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f5d09-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="f5d09-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f5d09-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="f5d09-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f5d09-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


