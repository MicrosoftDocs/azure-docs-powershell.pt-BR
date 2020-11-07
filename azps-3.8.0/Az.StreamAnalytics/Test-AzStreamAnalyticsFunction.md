---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777904"
---
# <span data-ttu-id="c9828-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c9828-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="c9828-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9828-102">SYNOPSIS</span></span>
<span data-ttu-id="c9828-103">Testa se o Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="c9828-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="c9828-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9828-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9828-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9828-105">DESCRIPTION</span></span>
<span data-ttu-id="c9828-106">O cmdlet **Test-AzStreamAnalyticsFunction** testa se o Azure Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="c9828-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="c9828-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9828-107">EXAMPLES</span></span>

### <span data-ttu-id="c9828-108">Exemplo 1: testar uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="c9828-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="c9828-109">Esse comando testa o status de conexão da função chamada ScoreTweet no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="c9828-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="c9828-110">OS</span><span class="sxs-lookup"><span data-stu-id="c9828-110">PARAMETERS</span></span>

### <span data-ttu-id="c9828-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9828-111">-DefaultProfile</span></span>
<span data-ttu-id="c9828-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9828-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9828-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="c9828-113">-JobName</span></span>
<span data-ttu-id="c9828-114">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="c9828-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="c9828-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9828-115">-Name</span></span>
<span data-ttu-id="c9828-116">Especifica o nome da função do Stream Analytics testada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9828-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="c9828-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9828-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9828-118">Especifica o nome do grupo de recursos ao qual a função Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="c9828-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="c9828-119">Esse cmdlet testa uma função no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c9828-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c9828-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9828-120">CommonParameters</span></span>
<span data-ttu-id="c9828-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9828-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9828-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9828-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9828-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9828-123">INPUTS</span></span>

### <span data-ttu-id="c9828-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c9828-124">System.String</span></span>

## <span data-ttu-id="c9828-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9828-125">OUTPUTS</span></span>

### <span data-ttu-id="c9828-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9828-126">System.Boolean</span></span>

## <span data-ttu-id="c9828-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9828-127">NOTES</span></span>

## <span data-ttu-id="c9828-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9828-128">RELATED LINKS</span></span>

[<span data-ttu-id="c9828-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c9828-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="c9828-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c9828-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="c9828-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c9828-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


