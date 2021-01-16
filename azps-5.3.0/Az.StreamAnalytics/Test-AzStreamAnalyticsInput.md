---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272470"
---
# <span data-ttu-id="8a74a-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8a74a-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="8a74a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a74a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a74a-103">Testa o status de conexão de uma entrada.</span><span class="sxs-lookup"><span data-stu-id="8a74a-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="8a74a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a74a-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a74a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a74a-105">DESCRIPTION</span></span>
<span data-ttu-id="8a74a-106">O cmdlet **Test-AzStreamAnalyticsInput** testa a capacidade do Stream Analytics de se conectar a uma entrada.</span><span class="sxs-lookup"><span data-stu-id="8a74a-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="8a74a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a74a-107">EXAMPLES</span></span>

### <span data-ttu-id="8a74a-108">Exemplo 1: testar o status de conexão de um fluxo de entrada</span><span class="sxs-lookup"><span data-stu-id="8a74a-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="8a74a-109">Isso testa o status de conexão da entrada EntryStream em StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="8a74a-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="8a74a-110">OS</span><span class="sxs-lookup"><span data-stu-id="8a74a-110">PARAMETERS</span></span>

### <span data-ttu-id="8a74a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a74a-111">-DefaultProfile</span></span>
<span data-ttu-id="8a74a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a74a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a74a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="8a74a-113">-JobName</span></span>
<span data-ttu-id="8a74a-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="8a74a-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="8a74a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a74a-115">-Name</span></span>
<span data-ttu-id="8a74a-116">Especifica o nome da entrada do Azure Stream Analytics para teste.</span><span class="sxs-lookup"><span data-stu-id="8a74a-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="8a74a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a74a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a74a-118">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="8a74a-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="8a74a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a74a-119">CommonParameters</span></span>
<span data-ttu-id="8a74a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a74a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a74a-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a74a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a74a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a74a-122">INPUTS</span></span>

### <span data-ttu-id="8a74a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8a74a-123">System.String</span></span>

## <span data-ttu-id="8a74a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a74a-124">OUTPUTS</span></span>

### <span data-ttu-id="8a74a-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a74a-125">System.Boolean</span></span>

## <span data-ttu-id="8a74a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a74a-126">NOTES</span></span>

## <span data-ttu-id="8a74a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a74a-127">RELATED LINKS</span></span>

[<span data-ttu-id="8a74a-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8a74a-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="8a74a-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8a74a-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="8a74a-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8a74a-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


