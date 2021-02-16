---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127135"
---
# <span data-ttu-id="8f73a-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="8f73a-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="8f73a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f73a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f73a-103">Obtém a saída de um trabalho de Automação.</span><span class="sxs-lookup"><span data-stu-id="8f73a-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="8f73a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f73a-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f73a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f73a-105">DESCRIPTION</span></span>
<span data-ttu-id="8f73a-106">O cmdlet **Get-AzAutomation JobOutput** obtém a saída de um trabalho de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f73a-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="8f73a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f73a-107">EXAMPLES</span></span>

### <span data-ttu-id="8f73a-108">Exemplo 1: Obter a saída de um trabalho de Automação</span><span class="sxs-lookup"><span data-stu-id="8f73a-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="8f73a-109">Esse comando obtém toda a saída do trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="8f73a-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="8f73a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f73a-110">PARAMETERS</span></span>

### <span data-ttu-id="8f73a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f73a-111">-AutomationAccountName</span></span>
<span data-ttu-id="8f73a-112">Especifica o nome de uma conta de Automação para a qual este cmdlet obtém a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f73a-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="8f73a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f73a-113">-DefaultProfile</span></span>
<span data-ttu-id="8f73a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8f73a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f73a-115">-ID</span><span class="sxs-lookup"><span data-stu-id="8f73a-115">-Id</span></span>
<span data-ttu-id="8f73a-116">Especifica a ID de um trabalho para o qual este cmdlet obtém saída.</span><span class="sxs-lookup"><span data-stu-id="8f73a-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f73a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f73a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f73a-118">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém a saída do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f73a-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="8f73a-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8f73a-119">-StartTime</span></span>
<span data-ttu-id="8f73a-120">Especifica uma hora de início como um **objeto DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="8f73a-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="8f73a-121">Você pode especificar uma cadeia de caracteres que pode ser convertida em **um DateTimeOffset válido.**</span><span class="sxs-lookup"><span data-stu-id="8f73a-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="8f73a-122">O cmdlet recupera a saída criada após esse período.</span><span class="sxs-lookup"><span data-stu-id="8f73a-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f73a-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="8f73a-123">-Stream</span></span>
<span data-ttu-id="8f73a-124">Especifica o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="8f73a-124">Specifies the type of output.</span></span>
<span data-ttu-id="8f73a-125">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="8f73a-125">Valid values are:</span></span> 
- <span data-ttu-id="8f73a-126">Qualquer</span><span class="sxs-lookup"><span data-stu-id="8f73a-126">Any</span></span>
- <span data-ttu-id="8f73a-127">Depurar</span><span class="sxs-lookup"><span data-stu-id="8f73a-127">Debug</span></span>
- <span data-ttu-id="8f73a-128">Erro</span><span class="sxs-lookup"><span data-stu-id="8f73a-128">Error</span></span>
- <span data-ttu-id="8f73a-129">Saída</span><span class="sxs-lookup"><span data-stu-id="8f73a-129">Output</span></span>
- <span data-ttu-id="8f73a-130">Progresso</span><span class="sxs-lookup"><span data-stu-id="8f73a-130">Progress</span></span>
- <span data-ttu-id="8f73a-131">Verbose</span><span class="sxs-lookup"><span data-stu-id="8f73a-131">Verbose</span></span>
- <span data-ttu-id="8f73a-132">Aviso</span><span class="sxs-lookup"><span data-stu-id="8f73a-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f73a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f73a-133">CommonParameters</span></span>
<span data-ttu-id="8f73a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f73a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f73a-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f73a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f73a-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f73a-136">INPUTS</span></span>

### <span data-ttu-id="8f73a-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8f73a-137">System.Guid</span></span>

### <span data-ttu-id="8f73a-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="8f73a-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="8f73a-139">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8f73a-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8f73a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8f73a-140">System.String</span></span>

## <span data-ttu-id="8f73a-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f73a-141">OUTPUTS</span></span>

### <span data-ttu-id="8f73a-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="8f73a-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="8f73a-143">Notas</span><span class="sxs-lookup"><span data-stu-id="8f73a-143">NOTES</span></span>

## <span data-ttu-id="8f73a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f73a-144">RELATED LINKS</span></span>

[<span data-ttu-id="8f73a-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8f73a-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="8f73a-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8f73a-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="8f73a-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8f73a-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="8f73a-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8f73a-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


