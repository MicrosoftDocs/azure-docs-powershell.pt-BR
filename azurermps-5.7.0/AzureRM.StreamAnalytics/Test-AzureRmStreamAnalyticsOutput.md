---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5e93638489749702a3da2608927318f794bc4a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432858"
---
# <span data-ttu-id="a25fc-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a25fc-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="a25fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a25fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a25fc-103">Testa o status de conexão de uma saída.</span><span class="sxs-lookup"><span data-stu-id="a25fc-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a25fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a25fc-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a25fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a25fc-105">DESCRIPTION</span></span>
<span data-ttu-id="a25fc-106">O cmdlet **Test-AzureRmStreamAnalyticsOutput** testa a capacidade do Stream Analytics de se conectar a uma saída.</span><span class="sxs-lookup"><span data-stu-id="a25fc-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="a25fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a25fc-107">EXAMPLES</span></span>

### <span data-ttu-id="a25fc-108">EXEMPLO 1: testar o status de conexão de uma saída</span><span class="sxs-lookup"><span data-stu-id="a25fc-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="a25fc-109">Isso testa o status de conexão da saída de saída em StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="a25fc-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="a25fc-110">OS</span><span class="sxs-lookup"><span data-stu-id="a25fc-110">PARAMETERS</span></span>

### <span data-ttu-id="a25fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25fc-111">-DefaultProfile</span></span>
<span data-ttu-id="a25fc-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a25fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a25fc-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="a25fc-113">-JobName</span></span>
<span data-ttu-id="a25fc-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a saída desejada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="a25fc-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="a25fc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a25fc-115">-Name</span></span>
<span data-ttu-id="a25fc-116">Especifica o nome da saída do Azure Stream Analytics para teste.</span><span class="sxs-lookup"><span data-stu-id="a25fc-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25fc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a25fc-117">-ResourceGroupName</span></span>
<span data-ttu-id="a25fc-118">Especifica o nome do grupo de recursos ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="a25fc-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="a25fc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25fc-119">CommonParameters</span></span>
<span data-ttu-id="a25fc-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25fc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25fc-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a25fc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25fc-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a25fc-122">INPUTS</span></span>

### <span data-ttu-id="a25fc-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a25fc-123">None</span></span>
<span data-ttu-id="a25fc-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a25fc-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a25fc-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a25fc-125">OUTPUTS</span></span>

### <span data-ttu-id="a25fc-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="a25fc-126">System.Object</span></span>

## <span data-ttu-id="a25fc-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a25fc-127">NOTES</span></span>

## <span data-ttu-id="a25fc-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a25fc-128">RELATED LINKS</span></span>

[<span data-ttu-id="a25fc-129">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a25fc-129">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="a25fc-130">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a25fc-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="a25fc-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a25fc-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


