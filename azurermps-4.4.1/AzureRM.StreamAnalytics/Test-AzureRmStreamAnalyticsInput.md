---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d0357e06257ad1df97b47ea7be59a1797e0f6902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603084"
---
# <span data-ttu-id="50405-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="50405-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="50405-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50405-102">SYNOPSIS</span></span>
<span data-ttu-id="50405-103">Testa o status de conexão de uma entrada.</span><span class="sxs-lookup"><span data-stu-id="50405-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50405-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50405-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50405-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50405-105">DESCRIPTION</span></span>
<span data-ttu-id="50405-106">O cmdlet **Test-AzureRmStreamAnalyticsInput** testa a capacidade do Stream Analytics de se conectar a uma entrada.</span><span class="sxs-lookup"><span data-stu-id="50405-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="50405-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50405-107">EXAMPLES</span></span>

### <span data-ttu-id="50405-108">EXEMPLO 1: testar o status de conexão de um fluxo de entrada</span><span class="sxs-lookup"><span data-stu-id="50405-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="50405-109">Isso testa o status de conexão da entrada EntryStream em StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="50405-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="50405-110">OS</span><span class="sxs-lookup"><span data-stu-id="50405-110">PARAMETERS</span></span>

### <span data-ttu-id="50405-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="50405-111">-JobName</span></span>
<span data-ttu-id="50405-112">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="50405-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="50405-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="50405-113">-Name</span></span>
<span data-ttu-id="50405-114">Especifica o nome da entrada do Azure Stream Analytics para teste.</span><span class="sxs-lookup"><span data-stu-id="50405-114">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="50405-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50405-115">-ResourceGroupName</span></span>
<span data-ttu-id="50405-116">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="50405-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="50405-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50405-117">-DefaultProfile</span></span>
<span data-ttu-id="50405-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50405-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50405-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50405-119">CommonParameters</span></span>
<span data-ttu-id="50405-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50405-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50405-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50405-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50405-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50405-122">INPUTS</span></span>

## <span data-ttu-id="50405-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50405-123">OUTPUTS</span></span>

### <span data-ttu-id="50405-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="50405-124">System.Object</span></span>

## <span data-ttu-id="50405-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50405-125">NOTES</span></span>

## <span data-ttu-id="50405-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50405-126">RELATED LINKS</span></span>

[<span data-ttu-id="50405-127">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="50405-127">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="50405-128">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="50405-128">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="50405-129">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="50405-129">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


