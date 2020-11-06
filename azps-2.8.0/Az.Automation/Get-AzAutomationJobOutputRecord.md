---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: f5c6976ca1fa398c38f642cef757f0e7956f40c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597843"
---
# <span data-ttu-id="022dd-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="022dd-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="022dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="022dd-102">SYNOPSIS</span></span>
<span data-ttu-id="022dd-103">Obtém a saída completa de um registro de saída do trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="022dd-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="022dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="022dd-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="022dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="022dd-105">DESCRIPTION</span></span>
<span data-ttu-id="022dd-106">O cmdlet **Get-AzAutomationJobOutputRecord** Obtém a saída completa de um registro de saída do trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="022dd-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="022dd-107">Embora o cmdlet **Get-AzAutomationJobOutput** liste um ou mais registros de saída de trabalho, ele retorna apenas um resumo, como uma cadeia de caracteres, do valor de qualquer registro de saída.</span><span class="sxs-lookup"><span data-stu-id="022dd-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="022dd-108">Ele não retorna o valor completo de um valor de saída de um registro de saída em seu tipo original.</span><span class="sxs-lookup"><span data-stu-id="022dd-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="022dd-109">Além disso, o resumo tem um comprimento máximo, que o valor total que este cmdlet gera pode exceder.</span><span class="sxs-lookup"><span data-stu-id="022dd-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="022dd-110">Ao contrário de **Get-AzAutomationJobOutput** , esse cmdlet retorna o valor completo em seu tipo originalmente reemitida, para qualquer valor de saída de registro de saída.</span><span class="sxs-lookup"><span data-stu-id="022dd-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="022dd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="022dd-111">EXAMPLES</span></span>

### <span data-ttu-id="022dd-112">Exemplo 1: obter a saída completa de um trabalho de automação</span><span class="sxs-lookup"><span data-stu-id="022dd-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="022dd-113">Esse comando obtém a saída completa do trabalho que tem a ID do trabalho especificada.</span><span class="sxs-lookup"><span data-stu-id="022dd-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="022dd-114">OS</span><span class="sxs-lookup"><span data-stu-id="022dd-114">PARAMETERS</span></span>

### <span data-ttu-id="022dd-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="022dd-115">-AutomationAccountName</span></span>
<span data-ttu-id="022dd-116">Especifica o nome de uma conta de automação para a qual esse cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="022dd-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="022dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="022dd-117">-DefaultProfile</span></span>
<span data-ttu-id="022dd-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="022dd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="022dd-119">-ID</span><span class="sxs-lookup"><span data-stu-id="022dd-119">-Id</span></span>
<span data-ttu-id="022dd-120">Especifica a ID de um registro de saída de trabalho para esse cmdlet ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="022dd-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="022dd-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="022dd-121">-JobId</span></span>
<span data-ttu-id="022dd-122">Especifica a ID de um trabalho para o qual esse cmdlet obtém um registro de saída.</span><span class="sxs-lookup"><span data-stu-id="022dd-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="022dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="022dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="022dd-124">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="022dd-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="022dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="022dd-125">CommonParameters</span></span>
<span data-ttu-id="022dd-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="022dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="022dd-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="022dd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="022dd-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="022dd-128">INPUTS</span></span>

### <span data-ttu-id="022dd-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="022dd-129">System.Guid</span></span>

### <span data-ttu-id="022dd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="022dd-130">System.String</span></span>

## <span data-ttu-id="022dd-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="022dd-131">OUTPUTS</span></span>

### <span data-ttu-id="022dd-132">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="022dd-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="022dd-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="022dd-133">NOTES</span></span>

## <span data-ttu-id="022dd-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="022dd-134">RELATED LINKS</span></span>

[<span data-ttu-id="022dd-135">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="022dd-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


