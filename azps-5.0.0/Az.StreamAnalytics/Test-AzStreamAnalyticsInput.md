---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117151"
---
# <span data-ttu-id="59f9d-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="59f9d-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="59f9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="59f9d-103">Testa o status de conexão de uma entrada.</span><span class="sxs-lookup"><span data-stu-id="59f9d-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="59f9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59f9d-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59f9d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="59f9d-106">O cmdlet **Test-AzStreamAnalyticsInput** testa a capacidade do Stream Analytics de se conectar a uma entrada.</span><span class="sxs-lookup"><span data-stu-id="59f9d-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="59f9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="59f9d-108">Exemplo 1: testar o status de conexão de um fluxo de entrada</span><span class="sxs-lookup"><span data-stu-id="59f9d-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="59f9d-109">Isso testa o status de conexão da entrada EntryStream em StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="59f9d-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="59f9d-110">OS</span><span class="sxs-lookup"><span data-stu-id="59f9d-110">PARAMETERS</span></span>

### <span data-ttu-id="59f9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f9d-111">-DefaultProfile</span></span>
<span data-ttu-id="59f9d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59f9d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59f9d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="59f9d-113">-JobName</span></span>
<span data-ttu-id="59f9d-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="59f9d-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="59f9d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="59f9d-115">-Name</span></span>
<span data-ttu-id="59f9d-116">Especifica o nome da entrada do Azure Stream Analytics para teste.</span><span class="sxs-lookup"><span data-stu-id="59f9d-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="59f9d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f9d-117">-ResourceGroupName</span></span>
<span data-ttu-id="59f9d-118">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="59f9d-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="59f9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f9d-119">CommonParameters</span></span>
<span data-ttu-id="59f9d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f9d-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f9d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f9d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59f9d-122">INPUTS</span></span>

### <span data-ttu-id="59f9d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="59f9d-123">System.String</span></span>

## <span data-ttu-id="59f9d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59f9d-124">OUTPUTS</span></span>

### <span data-ttu-id="59f9d-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59f9d-125">System.Boolean</span></span>

## <span data-ttu-id="59f9d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59f9d-126">NOTES</span></span>

## <span data-ttu-id="59f9d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59f9d-127">RELATED LINKS</span></span>

[<span data-ttu-id="59f9d-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="59f9d-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="59f9d-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="59f9d-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="59f9d-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="59f9d-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


