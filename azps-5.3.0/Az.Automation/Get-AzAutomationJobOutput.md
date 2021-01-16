---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432598"
---
# <span data-ttu-id="058fb-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="058fb-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="058fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="058fb-102">SYNOPSIS</span></span>
<span data-ttu-id="058fb-103">Obtém a saída de um trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="058fb-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="058fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="058fb-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="058fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="058fb-105">DESCRIPTION</span></span>
<span data-ttu-id="058fb-106">O cmdlet **Get-AzAutomationJobOutput** Obtém a saída de um trabalho de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="058fb-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="058fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="058fb-107">EXAMPLES</span></span>

### <span data-ttu-id="058fb-108">Exemplo 1: obter a saída de um trabalho de automação</span><span class="sxs-lookup"><span data-stu-id="058fb-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="058fb-109">Esse comando obtém toda a saída do trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="058fb-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="058fb-110">OS</span><span class="sxs-lookup"><span data-stu-id="058fb-110">PARAMETERS</span></span>

### <span data-ttu-id="058fb-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="058fb-111">-AutomationAccountName</span></span>
<span data-ttu-id="058fb-112">Especifica o nome de uma conta de automação para a qual esse cmdlet obtém a saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="058fb-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="058fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058fb-113">-DefaultProfile</span></span>
<span data-ttu-id="058fb-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="058fb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="058fb-115">-ID</span><span class="sxs-lookup"><span data-stu-id="058fb-115">-Id</span></span>
<span data-ttu-id="058fb-116">Especifica a ID de um trabalho para o qual esse cmdlet é uma saída.</span><span class="sxs-lookup"><span data-stu-id="058fb-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="058fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="058fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="058fb-118">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém a saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="058fb-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="058fb-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="058fb-119">-StartTime</span></span>
<span data-ttu-id="058fb-120">Especifica uma hora de início como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="058fb-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="058fb-121">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="058fb-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="058fb-122">O cmdlet recupera a saída criada após esse período.</span><span class="sxs-lookup"><span data-stu-id="058fb-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="058fb-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="058fb-123">-Stream</span></span>
<span data-ttu-id="058fb-124">Especifica o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="058fb-124">Specifies the type of output.</span></span>
<span data-ttu-id="058fb-125">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="058fb-125">Valid values are:</span></span> 
- <span data-ttu-id="058fb-126">Qualquer</span><span class="sxs-lookup"><span data-stu-id="058fb-126">Any</span></span>
- <span data-ttu-id="058fb-127">Depurá</span><span class="sxs-lookup"><span data-stu-id="058fb-127">Debug</span></span>
- <span data-ttu-id="058fb-128">Erros</span><span class="sxs-lookup"><span data-stu-id="058fb-128">Error</span></span>
- <span data-ttu-id="058fb-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="058fb-129">Output</span></span>
- <span data-ttu-id="058fb-130">Progresso</span><span class="sxs-lookup"><span data-stu-id="058fb-130">Progress</span></span>
- <span data-ttu-id="058fb-131">Detalha</span><span class="sxs-lookup"><span data-stu-id="058fb-131">Verbose</span></span>
- <span data-ttu-id="058fb-132">Avisa</span><span class="sxs-lookup"><span data-stu-id="058fb-132">Warning</span></span>

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

### <span data-ttu-id="058fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058fb-133">CommonParameters</span></span>
<span data-ttu-id="058fb-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="058fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058fb-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="058fb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058fb-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="058fb-136">INPUTS</span></span>

### <span data-ttu-id="058fb-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="058fb-137">System.Guid</span></span>

### <span data-ttu-id="058fb-138">Microsoft. Azure. Commands. Automation. Common. Streamtype</span><span class="sxs-lookup"><span data-stu-id="058fb-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="058fb-139">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="058fb-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="058fb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="058fb-140">System.String</span></span>

## <span data-ttu-id="058fb-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="058fb-141">OUTPUTS</span></span>

### <span data-ttu-id="058fb-142">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="058fb-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="058fb-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="058fb-143">NOTES</span></span>

## <span data-ttu-id="058fb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="058fb-144">RELATED LINKS</span></span>

[<span data-ttu-id="058fb-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="058fb-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="058fb-146">Currículo-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="058fb-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="058fb-147">Parar-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="058fb-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="058fb-148">Suspender-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="058fb-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


