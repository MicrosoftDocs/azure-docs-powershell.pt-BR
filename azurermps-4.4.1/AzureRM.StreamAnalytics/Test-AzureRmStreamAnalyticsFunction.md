---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: a2f577286a411287886c27863eb72e574b771bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603088"
---
# <span data-ttu-id="854b7-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="854b7-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="854b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="854b7-102">SYNOPSIS</span></span>
<span data-ttu-id="854b7-103">Testa se o Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="854b7-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="854b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="854b7-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="854b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="854b7-105">DESCRIPTION</span></span>
<span data-ttu-id="854b7-106">O cmdlet **Test-AzureRmStreamAnalyticsFunction** testa se o Azure Stream Analytics pode se conectar a uma função.</span><span class="sxs-lookup"><span data-stu-id="854b7-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="854b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="854b7-107">EXAMPLES</span></span>

### <span data-ttu-id="854b7-108">Exemplo 1: testar uma função do Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="854b7-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="854b7-109">Esse comando testa o status de conexão da função chamada ScoreTweet no trabalho chamado StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="854b7-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="854b7-110">OS</span><span class="sxs-lookup"><span data-stu-id="854b7-110">PARAMETERS</span></span>

### <span data-ttu-id="854b7-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="854b7-111">-JobName</span></span>
<span data-ttu-id="854b7-112">Especifica o nome do trabalho do Stream Analytics ao qual uma função pertence.</span><span class="sxs-lookup"><span data-stu-id="854b7-112">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="854b7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="854b7-113">-Name</span></span>
<span data-ttu-id="854b7-114">Especifica o nome da função do Stream Analytics testada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="854b7-114">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="854b7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="854b7-115">-ResourceGroupName</span></span>
<span data-ttu-id="854b7-116">Especifica o nome do grupo de recursos ao qual a função Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="854b7-116">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="854b7-117">Esse cmdlet testa uma função no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="854b7-117">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="854b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="854b7-118">-DefaultProfile</span></span>
<span data-ttu-id="854b7-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="854b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="854b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854b7-120">CommonParameters</span></span>
<span data-ttu-id="854b7-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="854b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854b7-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="854b7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854b7-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="854b7-123">INPUTS</span></span>

## <span data-ttu-id="854b7-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="854b7-124">OUTPUTS</span></span>

### <span data-ttu-id="854b7-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="854b7-125">System.Object</span></span>

## <span data-ttu-id="854b7-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="854b7-126">NOTES</span></span>

## <span data-ttu-id="854b7-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="854b7-127">RELATED LINKS</span></span>

[<span data-ttu-id="854b7-128">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="854b7-128">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="854b7-129">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="854b7-129">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="854b7-130">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="854b7-130">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)


