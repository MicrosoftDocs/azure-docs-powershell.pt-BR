---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112441"
---
# <span data-ttu-id="aecad-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="aecad-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="aecad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aecad-102">SYNOPSIS</span></span>
<span data-ttu-id="aecad-103">Testa o status de conexão de uma entrada.</span><span class="sxs-lookup"><span data-stu-id="aecad-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="aecad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aecad-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aecad-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="aecad-105">DESCRIPTION</span></span>
<span data-ttu-id="aecad-106">O cmdlet **Test-AzStreamAnalyticsInput** testa a capacidade do Stream Analytics de se conectar a uma entrada.</span><span class="sxs-lookup"><span data-stu-id="aecad-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="aecad-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aecad-107">EXAMPLES</span></span>

### <span data-ttu-id="aecad-108">Exemplo 1: Testar o status da conexão de um fluxo de entrada</span><span class="sxs-lookup"><span data-stu-id="aecad-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="aecad-109">Isso testa o status de conexão da EntradaStream de entrada no StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="aecad-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="aecad-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aecad-110">PARAMETERS</span></span>

### <span data-ttu-id="aecad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aecad-111">-DefaultProfile</span></span>
<span data-ttu-id="aecad-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="aecad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aecad-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="aecad-113">-JobName</span></span>
<span data-ttu-id="aecad-114">Especifica o nome do trabalho do Azure Stream Analytics ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="aecad-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="aecad-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="aecad-115">-Name</span></span>
<span data-ttu-id="aecad-116">Especifica o nome da entrada do Azure Stream Analytics para teste.</span><span class="sxs-lookup"><span data-stu-id="aecad-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="aecad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aecad-117">-ResourceGroupName</span></span>
<span data-ttu-id="aecad-118">Especifica o nome do grupo de recursos ao qual a entrada do Azure Stream Analytics pertence.</span><span class="sxs-lookup"><span data-stu-id="aecad-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="aecad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecad-119">CommonParameters</span></span>
<span data-ttu-id="aecad-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aecad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecad-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aecad-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecad-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="aecad-122">INPUTS</span></span>

### <span data-ttu-id="aecad-123">System.String</span><span class="sxs-lookup"><span data-stu-id="aecad-123">System.String</span></span>

## <span data-ttu-id="aecad-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="aecad-124">OUTPUTS</span></span>

### <span data-ttu-id="aecad-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aecad-125">System.Boolean</span></span>

## <span data-ttu-id="aecad-126">Notas</span><span class="sxs-lookup"><span data-stu-id="aecad-126">NOTES</span></span>

## <span data-ttu-id="aecad-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aecad-127">RELATED LINKS</span></span>

[<span data-ttu-id="aecad-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="aecad-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="aecad-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="aecad-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="aecad-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="aecad-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


