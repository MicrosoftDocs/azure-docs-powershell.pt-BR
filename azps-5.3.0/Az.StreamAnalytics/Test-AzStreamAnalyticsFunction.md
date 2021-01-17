---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432909"
---
# <span data-ttu-id="564f3-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="564f3-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="564f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="564f3-102">SYNOPSIS</span></span>
<span data-ttu-id="564f3-103">Testa se o Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="564f3-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="564f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="564f3-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="564f3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="564f3-105">DESCRIPTION</span></span>
<span data-ttu-id="564f3-106">O cmdlet **Test-AzStreamAnalyticsFunction** testa se o Azure Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="564f3-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="564f3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="564f3-107">EXAMPLES</span></span>

### <span data-ttu-id="564f3-108">Exemplo 1: testar uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="564f3-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="564f3-109">Esse comando testa o status de conexão da função chamada ScoreTweet no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="564f3-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="564f3-110">OS</span><span class="sxs-lookup"><span data-stu-id="564f3-110">PARAMETERS</span></span>

### <span data-ttu-id="564f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564f3-111">-DefaultProfile</span></span>
<span data-ttu-id="564f3-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="564f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="564f3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="564f3-113">-JobName</span></span>
<span data-ttu-id="564f3-114">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="564f3-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="564f3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="564f3-115">-Name</span></span>
<span data-ttu-id="564f3-116">Especifica o nome da função do Stream Analytics testada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="564f3-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="564f3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="564f3-117">-ResourceGroupName</span></span>
<span data-ttu-id="564f3-118">Especifica o nome do grupo de recursos ao qual a função Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="564f3-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="564f3-119">Esse cmdlet testa uma função no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="564f3-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="564f3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564f3-120">CommonParameters</span></span>
<span data-ttu-id="564f3-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="564f3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564f3-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="564f3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564f3-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="564f3-123">INPUTS</span></span>

### <span data-ttu-id="564f3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="564f3-124">System.String</span></span>

## <span data-ttu-id="564f3-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="564f3-125">OUTPUTS</span></span>

### <span data-ttu-id="564f3-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="564f3-126">System.Boolean</span></span>

## <span data-ttu-id="564f3-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="564f3-127">NOTES</span></span>

## <span data-ttu-id="564f3-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="564f3-128">RELATED LINKS</span></span>

[<span data-ttu-id="564f3-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="564f3-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="564f3-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="564f3-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="564f3-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="564f3-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


