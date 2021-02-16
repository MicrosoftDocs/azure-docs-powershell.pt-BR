---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127129"
---
# <span data-ttu-id="11c32-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="11c32-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="11c32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11c32-102">SYNOPSIS</span></span>
<span data-ttu-id="11c32-103">Obtém a saída total de um registro de saída de trabalho automação.</span><span class="sxs-lookup"><span data-stu-id="11c32-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="11c32-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11c32-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11c32-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="11c32-105">DESCRIPTION</span></span>
<span data-ttu-id="11c32-106">O cmdlet **Get-AzAutomation JobOutputRecord** obtém a saída total de um registro de saída de trabalho automação.</span><span class="sxs-lookup"><span data-stu-id="11c32-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="11c32-107">Embora o cmdlet **Get-AzAutomation JobOutput** lista um ou mais registros de saída de trabalho, ele retorna apenas um resumo, como uma cadeia de caracteres, do valor de qualquer registro de saída.</span><span class="sxs-lookup"><span data-stu-id="11c32-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="11c32-108">Ele não retorna o valor completo do valor de saída de um registro de saída em seu tipo original.</span><span class="sxs-lookup"><span data-stu-id="11c32-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="11c32-109">Além disso, o resumo tem um comprimento máximo, que o valor total que as saídas desse cmdlet podem exceder.</span><span class="sxs-lookup"><span data-stu-id="11c32-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="11c32-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11c32-110">EXAMPLES</span></span>

### <span data-ttu-id="11c32-111">Exemplo 1: Obter a saída completa de um trabalho de Automação</span><span class="sxs-lookup"><span data-stu-id="11c32-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="11c32-112">Esse comando obtém a saída completa do trabalho que tem a ID de trabalho especificada.</span><span class="sxs-lookup"><span data-stu-id="11c32-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="11c32-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11c32-113">PARAMETERS</span></span>

### <span data-ttu-id="11c32-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11c32-114">-AutomationAccountName</span></span>
<span data-ttu-id="11c32-115">Especifica o nome de uma conta de Automação para a qual este cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="11c32-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="11c32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c32-116">-DefaultProfile</span></span>
<span data-ttu-id="11c32-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="11c32-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11c32-118">-ID</span><span class="sxs-lookup"><span data-stu-id="11c32-118">-Id</span></span>
<span data-ttu-id="11c32-119">Especifica a ID de um registro de saída de trabalho para que este cmdlet seja recuperado.</span><span class="sxs-lookup"><span data-stu-id="11c32-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="11c32-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="11c32-120">-JobId</span></span>
<span data-ttu-id="11c32-121">Especifica a ID de um trabalho para o qual este cmdlet obtém um registro de saída.</span><span class="sxs-lookup"><span data-stu-id="11c32-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="11c32-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c32-122">-ResourceGroupName</span></span>
<span data-ttu-id="11c32-123">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém um registro de saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="11c32-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="11c32-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c32-124">CommonParameters</span></span>
<span data-ttu-id="11c32-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c32-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c32-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11c32-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c32-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="11c32-127">INPUTS</span></span>

### <span data-ttu-id="11c32-128">System.Guid</span><span class="sxs-lookup"><span data-stu-id="11c32-128">System.Guid</span></span>

### <span data-ttu-id="11c32-129">System.String</span><span class="sxs-lookup"><span data-stu-id="11c32-129">System.String</span></span>

## <span data-ttu-id="11c32-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="11c32-130">OUTPUTS</span></span>

### <span data-ttu-id="11c32-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="11c32-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="11c32-132">Notas</span><span class="sxs-lookup"><span data-stu-id="11c32-132">NOTES</span></span>

## <span data-ttu-id="11c32-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11c32-133">RELATED LINKS</span></span>

[<span data-ttu-id="11c32-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="11c32-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


