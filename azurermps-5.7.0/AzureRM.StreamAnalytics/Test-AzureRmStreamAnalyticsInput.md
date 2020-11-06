---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 34e1c2813292801d29a93a6914abf11b2725ec14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427392"
---
# <span data-ttu-id="aa21a-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="aa21a-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="aa21a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa21a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa21a-103">Testa o status de conexão de uma entrada.</span><span class="sxs-lookup"><span data-stu-id="aa21a-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa21a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa21a-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa21a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa21a-105">DESCRIPTION</span></span>
<span data-ttu-id="aa21a-106">O cmdlet **Test-AzureRmStreamAnalyticsInput** testa a capacidade do Stream Analytics de se conectar a uma entrada.</span><span class="sxs-lookup"><span data-stu-id="aa21a-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="aa21a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa21a-107">EXAMPLES</span></span>

### <span data-ttu-id="aa21a-108">EXEMPLO 1: testar o status de conexão de um fluxo de entrada</span><span class="sxs-lookup"><span data-stu-id="aa21a-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="aa21a-109">Isso testa o status de conexão da entrada EntryStream em StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="aa21a-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="aa21a-110">OS</span><span class="sxs-lookup"><span data-stu-id="aa21a-110">PARAMETERS</span></span>

### <span data-ttu-id="aa21a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa21a-111">-DefaultProfile</span></span>
<span data-ttu-id="aa21a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa21a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa21a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="aa21a-113">-JobName</span></span>
<span data-ttu-id="aa21a-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="aa21a-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="aa21a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa21a-115">-Name</span></span>
<span data-ttu-id="aa21a-116">Especifica o nome da entrada do Azure Stream Analytics para teste.</span><span class="sxs-lookup"><span data-stu-id="aa21a-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="aa21a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa21a-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa21a-118">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="aa21a-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="aa21a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa21a-119">CommonParameters</span></span>
<span data-ttu-id="aa21a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa21a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa21a-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa21a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa21a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa21a-122">INPUTS</span></span>

### <span data-ttu-id="aa21a-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="aa21a-123">None</span></span>
<span data-ttu-id="aa21a-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="aa21a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa21a-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa21a-125">OUTPUTS</span></span>

### <span data-ttu-id="aa21a-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="aa21a-126">System.Object</span></span>

## <span data-ttu-id="aa21a-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa21a-127">NOTES</span></span>

## <span data-ttu-id="aa21a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa21a-128">RELATED LINKS</span></span>

[<span data-ttu-id="aa21a-129">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="aa21a-129">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="aa21a-130">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="aa21a-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="aa21a-131">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="aa21a-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


