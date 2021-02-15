---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112442"
---
# <span data-ttu-id="872b5-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="872b5-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="872b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="872b5-102">SYNOPSIS</span></span>
<span data-ttu-id="872b5-103">Testa se o Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="872b5-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="872b5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="872b5-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="872b5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="872b5-105">DESCRIPTION</span></span>
<span data-ttu-id="872b5-106">O cmdlet **Test-AzStreamAnalyticsFunction** testa se o Azure Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="872b5-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="872b5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="872b5-107">EXAMPLES</span></span>

### <span data-ttu-id="872b5-108">Exemplo 1: Testar uma função Análise de Fluxo</span><span class="sxs-lookup"><span data-stu-id="872b5-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="872b5-109">Este comando testa o status de conexão da função chamada ScoreTweet no trabalho chamado Stream Job22.</span><span class="sxs-lookup"><span data-stu-id="872b5-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="872b5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="872b5-110">PARAMETERS</span></span>

### <span data-ttu-id="872b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872b5-111">-DefaultProfile</span></span>
<span data-ttu-id="872b5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="872b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="872b5-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="872b5-113">-JobName</span></span>
<span data-ttu-id="872b5-114">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="872b5-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="872b5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="872b5-115">-Name</span></span>
<span data-ttu-id="872b5-116">Especifica o nome da função Análise de Fluxo que este cmdlet testa.</span><span class="sxs-lookup"><span data-stu-id="872b5-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="872b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="872b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="872b5-118">Especifica o nome do grupo de recursos ao qual uma função de Análise de Fluxo pertence.</span><span class="sxs-lookup"><span data-stu-id="872b5-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="872b5-119">Este cmdlet testa uma função no grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="872b5-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="872b5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872b5-120">CommonParameters</span></span>
<span data-ttu-id="872b5-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="872b5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872b5-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872b5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872b5-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="872b5-123">INPUTS</span></span>

### <span data-ttu-id="872b5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="872b5-124">System.String</span></span>

## <span data-ttu-id="872b5-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="872b5-125">OUTPUTS</span></span>

### <span data-ttu-id="872b5-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="872b5-126">System.Boolean</span></span>

## <span data-ttu-id="872b5-127">Notas</span><span class="sxs-lookup"><span data-stu-id="872b5-127">NOTES</span></span>

## <span data-ttu-id="872b5-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="872b5-128">RELATED LINKS</span></span>

[<span data-ttu-id="872b5-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="872b5-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="872b5-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="872b5-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="872b5-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="872b5-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


