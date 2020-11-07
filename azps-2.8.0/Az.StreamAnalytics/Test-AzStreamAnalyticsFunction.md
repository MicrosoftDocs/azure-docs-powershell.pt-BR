---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: f9139514850fe9d538c58d14813e91d2d24de502
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774261"
---
# <span data-ttu-id="2749b-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2749b-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="2749b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2749b-102">SYNOPSIS</span></span>
<span data-ttu-id="2749b-103">Testa se o Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="2749b-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="2749b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2749b-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2749b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2749b-105">DESCRIPTION</span></span>
<span data-ttu-id="2749b-106">O cmdlet **Test-AzStreamAnalyticsFunction** testa se o Azure Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="2749b-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="2749b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2749b-107">EXAMPLES</span></span>

### <span data-ttu-id="2749b-108">Exemplo 1: testar uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="2749b-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="2749b-109">Esse comando testa o status de conexão da função chamada ScoreTweet no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="2749b-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="2749b-110">OS</span><span class="sxs-lookup"><span data-stu-id="2749b-110">PARAMETERS</span></span>

### <span data-ttu-id="2749b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2749b-111">-DefaultProfile</span></span>
<span data-ttu-id="2749b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2749b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2749b-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="2749b-113">-JobName</span></span>
<span data-ttu-id="2749b-114">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="2749b-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="2749b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2749b-115">-Name</span></span>
<span data-ttu-id="2749b-116">Especifica o nome da função do Stream Analytics testada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2749b-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="2749b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2749b-117">-ResourceGroupName</span></span>
<span data-ttu-id="2749b-118">Especifica o nome do grupo de recursos ao qual a função Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="2749b-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="2749b-119">Esse cmdlet testa uma função no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2749b-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2749b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2749b-120">CommonParameters</span></span>
<span data-ttu-id="2749b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2749b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2749b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2749b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2749b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2749b-123">INPUTS</span></span>

### <span data-ttu-id="2749b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2749b-124">System.String</span></span>

## <span data-ttu-id="2749b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2749b-125">OUTPUTS</span></span>

### <span data-ttu-id="2749b-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2749b-126">System.Boolean</span></span>

## <span data-ttu-id="2749b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2749b-127">NOTES</span></span>

## <span data-ttu-id="2749b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2749b-128">RELATED LINKS</span></span>

[<span data-ttu-id="2749b-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2749b-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="2749b-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2749b-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="2749b-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2749b-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

