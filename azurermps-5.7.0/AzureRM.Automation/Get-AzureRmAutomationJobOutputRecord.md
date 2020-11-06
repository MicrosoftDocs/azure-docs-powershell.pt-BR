---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: 18551d6d839991cf0eb9e020c62fa0a24207d1e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431083"
---
# <span data-ttu-id="f006c-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="f006c-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="f006c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f006c-102">SYNOPSIS</span></span>
<span data-ttu-id="f006c-103">Obtém a saída completa de um registro de saída do trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="f006c-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f006c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f006c-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f006c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f006c-105">DESCRIPTION</span></span>
<span data-ttu-id="f006c-106">O cmdlet **Get-AzureRmAutomationJobOutputRecord** Obtém a saída completa de um registro de saída do trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="f006c-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>

<span data-ttu-id="f006c-107">Embora o cmdlet **Get-AzureRmAutomationJobOutput** liste um ou mais registros de saída de trabalho, ele retorna apenas um resumo, como uma cadeia de caracteres, do valor de qualquer registro de saída.</span><span class="sxs-lookup"><span data-stu-id="f006c-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="f006c-108">Ele não retorna o valor completo de um valor de saída de um registro de saída em seu tipo original.</span><span class="sxs-lookup"><span data-stu-id="f006c-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="f006c-109">Além disso, o resumo tem um comprimento máximo, que o valor total que este cmdlet gera pode exceder.</span><span class="sxs-lookup"><span data-stu-id="f006c-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="f006c-110">Ao contrário de **Get-AzureRmAutomationJobOutput** , esse cmdlet retorna o valor completo em seu tipo originalmente reemitida, para qualquer valor de saída de registro de saída.</span><span class="sxs-lookup"><span data-stu-id="f006c-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="f006c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f006c-111">EXAMPLES</span></span>

### <span data-ttu-id="f006c-112">Exemplo 1: obter a saída completa de um trabalho de automação</span><span class="sxs-lookup"><span data-stu-id="f006c-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="f006c-113">Esse comando obtém a saída completa do trabalho que tem a ID do trabalho especificada.</span><span class="sxs-lookup"><span data-stu-id="f006c-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="f006c-114">OS</span><span class="sxs-lookup"><span data-stu-id="f006c-114">PARAMETERS</span></span>

### <span data-ttu-id="f006c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f006c-115">-AutomationAccountName</span></span>
<span data-ttu-id="f006c-116">Especifica o nome de uma conta de automação para a qual esse cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f006c-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="f006c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f006c-117">-DefaultProfile</span></span>
<span data-ttu-id="f006c-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f006c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f006c-119">-ID</span><span class="sxs-lookup"><span data-stu-id="f006c-119">-Id</span></span>
<span data-ttu-id="f006c-120">Especifica a ID de um registro de saída de trabalho para esse cmdlet ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="f006c-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f006c-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="f006c-121">-JobId</span></span>
<span data-ttu-id="f006c-122">Especifica a ID de um trabalho para o qual esse cmdlet obtém um registro de saída.</span><span class="sxs-lookup"><span data-stu-id="f006c-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f006c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f006c-123">-ResourceGroupName</span></span>
<span data-ttu-id="f006c-124">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f006c-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="f006c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f006c-125">CommonParameters</span></span>
<span data-ttu-id="f006c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f006c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f006c-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f006c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f006c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f006c-128">INPUTS</span></span>

### <span data-ttu-id="f006c-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f006c-129">None</span></span>
<span data-ttu-id="f006c-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f006c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f006c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f006c-131">OUTPUTS</span></span>

### <span data-ttu-id="f006c-132">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="f006c-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="f006c-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f006c-133">NOTES</span></span>

## <span data-ttu-id="f006c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f006c-134">RELATED LINKS</span></span>

[<span data-ttu-id="f006c-135">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="f006c-135">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)


