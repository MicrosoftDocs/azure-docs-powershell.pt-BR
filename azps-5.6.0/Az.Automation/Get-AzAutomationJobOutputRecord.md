---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 2f4fd8c81cadd890cd17f2dd8d6db77c0eef5283
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891228"
---
# <span data-ttu-id="de311-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="de311-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="de311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de311-102">SYNOPSIS</span></span>
<span data-ttu-id="de311-103">Obtém a saída completa de um registro de saída de trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="de311-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="de311-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="de311-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de311-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="de311-105">DESCRIPTION</span></span>
<span data-ttu-id="de311-106">O cmdlet **Get-AzAutomationJobOutputRecord** obtém a saída completa de um registro de saída de trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="de311-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="de311-107">Embora o cmdlet **Get-AzAutomationJobOutput** lista um ou mais registros de saída de trabalho, ele retorna apenas um resumo, como uma cadeia de caracteres, do valor de qualquer registro de saída.</span><span class="sxs-lookup"><span data-stu-id="de311-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="de311-108">Ele não retorna o valor completo do valor de saída de um registro de saída em seu tipo original.</span><span class="sxs-lookup"><span data-stu-id="de311-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="de311-109">Além disso, o resumo tem um comprimento máximo, que o valor total que esse cmdlet pode exceder.</span><span class="sxs-lookup"><span data-stu-id="de311-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="de311-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de311-110">EXAMPLES</span></span>

### <span data-ttu-id="de311-111">Exemplo 1: Obter a saída completa de um trabalho de Automação</span><span class="sxs-lookup"><span data-stu-id="de311-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="de311-112">Este comando obtém a saída completa do trabalho que tem a ID de trabalho especificada.</span><span class="sxs-lookup"><span data-stu-id="de311-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="de311-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="de311-113">PARAMETERS</span></span>

### <span data-ttu-id="de311-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="de311-114">-AutomationAccountName</span></span>
<span data-ttu-id="de311-115">Especifica o nome de uma conta de Automação para a qual esse cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="de311-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="de311-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de311-116">-DefaultProfile</span></span>
<span data-ttu-id="de311-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="de311-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de311-118">-Id</span><span class="sxs-lookup"><span data-stu-id="de311-118">-Id</span></span>
<span data-ttu-id="de311-119">Especifica a ID de um registro de saída de trabalho para este cmdlet recuperar.</span><span class="sxs-lookup"><span data-stu-id="de311-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="de311-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="de311-120">-JobId</span></span>
<span data-ttu-id="de311-121">Especifica a ID de um trabalho para o qual este cmdlet obtém um registro de saída.</span><span class="sxs-lookup"><span data-stu-id="de311-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="de311-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de311-122">-ResourceGroupName</span></span>
<span data-ttu-id="de311-123">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="de311-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="de311-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de311-124">CommonParameters</span></span>
<span data-ttu-id="de311-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de311-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de311-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de311-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de311-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de311-127">INPUTS</span></span>

### <span data-ttu-id="de311-128">System.Guid</span><span class="sxs-lookup"><span data-stu-id="de311-128">System.Guid</span></span>

### <span data-ttu-id="de311-129">System.String</span><span class="sxs-lookup"><span data-stu-id="de311-129">System.String</span></span>

## <span data-ttu-id="de311-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="de311-130">OUTPUTS</span></span>

### <span data-ttu-id="de311-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="de311-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="de311-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="de311-132">NOTES</span></span>

## <span data-ttu-id="de311-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de311-133">RELATED LINKS</span></span>

[<span data-ttu-id="de311-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="de311-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


