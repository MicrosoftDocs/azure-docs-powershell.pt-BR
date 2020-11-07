---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 69e9d06a790fa473a278e50e79ad90be93f0527c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956084"
---
# <span data-ttu-id="0f1ec-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0f1ec-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="0f1ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="0f1ec-103">Testa o status de conexão de uma saída.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="0f1ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f1ec-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f1ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f1ec-105">DESCRIPTION</span></span>
<span data-ttu-id="0f1ec-106">O cmdlet **Test-AzStreamAnalyticsOutput** testa a capacidade do Stream Analytics de se conectar a uma saída.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="0f1ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f1ec-107">EXAMPLES</span></span>

### <span data-ttu-id="0f1ec-108">Exemplo 1: testar o status de conexão de uma saída</span><span class="sxs-lookup"><span data-stu-id="0f1ec-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="0f1ec-109">Isso testa o status de conexão da saída de saída em StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="0f1ec-110">OS</span><span class="sxs-lookup"><span data-stu-id="0f1ec-110">PARAMETERS</span></span>

### <span data-ttu-id="0f1ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f1ec-111">-DefaultProfile</span></span>
<span data-ttu-id="0f1ec-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f1ec-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0f1ec-113">-JobName</span></span>
<span data-ttu-id="0f1ec-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a saída desejada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0f1ec-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f1ec-115">-Name</span></span>
<span data-ttu-id="0f1ec-116">Especifica o nome da saída do Azure Stream Analytics para teste.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="0f1ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f1ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f1ec-118">Especifica o nome do grupo de recursos ao qual a saída do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0f1ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f1ec-119">CommonParameters</span></span>
<span data-ttu-id="0f1ec-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f1ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f1ec-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f1ec-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f1ec-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f1ec-122">INPUTS</span></span>

### <span data-ttu-id="0f1ec-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0f1ec-123">System.String</span></span>

## <span data-ttu-id="0f1ec-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f1ec-124">OUTPUTS</span></span>

### <span data-ttu-id="0f1ec-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f1ec-125">System.Boolean</span></span>

## <span data-ttu-id="0f1ec-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f1ec-126">NOTES</span></span>

## <span data-ttu-id="0f1ec-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f1ec-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f1ec-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0f1ec-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0f1ec-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0f1ec-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0f1ec-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0f1ec-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


