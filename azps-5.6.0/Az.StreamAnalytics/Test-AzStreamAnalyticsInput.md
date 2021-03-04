---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: 09cf95f6fd7feb17053063952ae7110098353c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891924"
---
# <span data-ttu-id="83345-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="83345-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="83345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83345-102">SYNOPSIS</span></span>
<span data-ttu-id="83345-103">Testa o status da conexão de uma entrada.</span><span class="sxs-lookup"><span data-stu-id="83345-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="83345-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="83345-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83345-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="83345-105">DESCRIPTION</span></span>
<span data-ttu-id="83345-106">O cmdlet **Test-AzStreamAnalyticsInput** testa a capacidade do Stream Analytics de se conectar a uma entrada.</span><span class="sxs-lookup"><span data-stu-id="83345-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="83345-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83345-107">EXAMPLES</span></span>

### <span data-ttu-id="83345-108">Exemplo 1: Testar o status de conexão de um fluxo de entrada</span><span class="sxs-lookup"><span data-stu-id="83345-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="83345-109">Isso testa o status de conexão da entrada EntryStream no StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="83345-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="83345-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="83345-110">PARAMETERS</span></span>

### <span data-ttu-id="83345-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83345-111">-DefaultProfile</span></span>
<span data-ttu-id="83345-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="83345-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83345-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="83345-113">-JobName</span></span>
<span data-ttu-id="83345-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="83345-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="83345-115">-Name</span><span class="sxs-lookup"><span data-stu-id="83345-115">-Name</span></span>
<span data-ttu-id="83345-116">Especifica o nome da entrada do Azure Stream Analytics a ser testado.</span><span class="sxs-lookup"><span data-stu-id="83345-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="83345-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83345-117">-ResourceGroupName</span></span>
<span data-ttu-id="83345-118">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="83345-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="83345-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83345-119">CommonParameters</span></span>
<span data-ttu-id="83345-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83345-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83345-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83345-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83345-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83345-122">INPUTS</span></span>

### <span data-ttu-id="83345-123">System.String</span><span class="sxs-lookup"><span data-stu-id="83345-123">System.String</span></span>

## <span data-ttu-id="83345-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="83345-124">OUTPUTS</span></span>

### <span data-ttu-id="83345-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83345-125">System.Boolean</span></span>

## <span data-ttu-id="83345-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="83345-126">NOTES</span></span>

## <span data-ttu-id="83345-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83345-127">RELATED LINKS</span></span>

[<span data-ttu-id="83345-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="83345-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="83345-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="83345-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="83345-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="83345-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


