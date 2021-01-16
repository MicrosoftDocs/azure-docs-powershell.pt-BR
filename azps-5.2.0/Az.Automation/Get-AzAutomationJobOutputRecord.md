---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264601"
---
# <span data-ttu-id="3c4c3-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="3c4c3-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="3c4c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c4c3-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4c3-103">Obtém a saída completa de um registro de saída do trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="3c4c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c4c3-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c4c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c4c3-105">DESCRIPTION</span></span>
<span data-ttu-id="3c4c3-106">O cmdlet **Get-AzAutomationJobOutputRecord** Obtém a saída completa de um registro de saída do trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="3c4c3-107">Embora o cmdlet **Get-AzAutomationJobOutput** liste um ou mais registros de saída de trabalho, ele retorna apenas um resumo, como uma cadeia de caracteres, do valor de qualquer registro de saída.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="3c4c3-108">Ele não retorna o valor completo de um valor de saída de um registro de saída em seu tipo original.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="3c4c3-109">Além disso, o resumo tem um comprimento máximo, que o valor total que este cmdlet gera pode exceder.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="3c4c3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c4c3-110">EXAMPLES</span></span>

### <span data-ttu-id="3c4c3-111">Exemplo 1: obter a saída completa de um trabalho de automação</span><span class="sxs-lookup"><span data-stu-id="3c4c3-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="3c4c3-112">Esse comando obtém a saída completa do trabalho que tem a ID do trabalho especificada.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="3c4c3-113">OS</span><span class="sxs-lookup"><span data-stu-id="3c4c3-113">PARAMETERS</span></span>

### <span data-ttu-id="3c4c3-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3c4c3-114">-AutomationAccountName</span></span>
<span data-ttu-id="3c4c3-115">Especifica o nome de uma conta de automação para a qual esse cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="3c4c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4c3-116">-DefaultProfile</span></span>
<span data-ttu-id="3c4c3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3c4c3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c4c3-118">-ID</span><span class="sxs-lookup"><span data-stu-id="3c4c3-118">-Id</span></span>
<span data-ttu-id="3c4c3-119">Especifica a ID de um registro de saída de trabalho para esse cmdlet ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c4c3-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="3c4c3-120">-JobId</span></span>
<span data-ttu-id="3c4c3-121">Especifica a ID de um trabalho para o qual esse cmdlet obtém um registro de saída.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c4c3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c4c3-122">-ResourceGroupName</span></span>
<span data-ttu-id="3c4c3-123">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="3c4c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4c3-124">CommonParameters</span></span>
<span data-ttu-id="3c4c3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c4c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4c3-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c4c3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4c3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c4c3-127">INPUTS</span></span>

### <span data-ttu-id="3c4c3-128">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3c4c3-128">System.Guid</span></span>

### <span data-ttu-id="3c4c3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3c4c3-129">System.String</span></span>

## <span data-ttu-id="3c4c3-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c4c3-130">OUTPUTS</span></span>

### <span data-ttu-id="3c4c3-131">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="3c4c3-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="3c4c3-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c4c3-132">NOTES</span></span>

## <span data-ttu-id="3c4c3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c4c3-133">RELATED LINKS</span></span>

[<span data-ttu-id="3c4c3-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="3c4c3-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


