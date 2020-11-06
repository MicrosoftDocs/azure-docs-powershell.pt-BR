---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: d46dd2e314aa8064b305adb0501ae20480a34418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602177"
---
# <span data-ttu-id="79443-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="79443-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="79443-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79443-102">SYNOPSIS</span></span>
<span data-ttu-id="79443-103">Obtém a saída de um trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="79443-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79443-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79443-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79443-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79443-105">DESCRIPTION</span></span>
<span data-ttu-id="79443-106">O cmdlet **Get-AzureRmAutomationJobOutput** Obtém a saída de um trabalho de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="79443-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="79443-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79443-107">EXAMPLES</span></span>

### <span data-ttu-id="79443-108">Exemplo 1: obter a saída de um trabalho de automação</span><span class="sxs-lookup"><span data-stu-id="79443-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="79443-109">Esse comando obtém toda a saída do trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="79443-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="79443-110">OS</span><span class="sxs-lookup"><span data-stu-id="79443-110">PARAMETERS</span></span>

### <span data-ttu-id="79443-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="79443-111">-AutomationAccountName</span></span>
<span data-ttu-id="79443-112">Especifica o nome de uma conta de automação para a qual esse cmdlet obtém a saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="79443-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="79443-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79443-113">-DefaultProfile</span></span>
<span data-ttu-id="79443-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="79443-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79443-115">-ID</span><span class="sxs-lookup"><span data-stu-id="79443-115">-Id</span></span>
<span data-ttu-id="79443-116">Especifica a ID de um trabalho para o qual esse cmdlet é uma saída.</span><span class="sxs-lookup"><span data-stu-id="79443-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79443-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79443-117">-ResourceGroupName</span></span>
<span data-ttu-id="79443-118">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém a saída de trabalho.</span><span class="sxs-lookup"><span data-stu-id="79443-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="79443-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="79443-119">-StartTime</span></span>
<span data-ttu-id="79443-120">Especifica uma hora de início como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="79443-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="79443-121">Você pode especificar uma cadeia de caracteres que pode ser convertida em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="79443-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="79443-122">O cmdlet recupera a saída criada após esse período.</span><span class="sxs-lookup"><span data-stu-id="79443-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79443-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="79443-123">-Stream</span></span>
<span data-ttu-id="79443-124">Especifica o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="79443-124">Specifies the type of output.</span></span>
<span data-ttu-id="79443-125">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="79443-125">Valid values are:</span></span> 

- <span data-ttu-id="79443-126">Qualquer</span><span class="sxs-lookup"><span data-stu-id="79443-126">Any</span></span>
- <span data-ttu-id="79443-127">Depurá</span><span class="sxs-lookup"><span data-stu-id="79443-127">Debug</span></span>
- <span data-ttu-id="79443-128">Erros</span><span class="sxs-lookup"><span data-stu-id="79443-128">Error</span></span>
- <span data-ttu-id="79443-129">Entrada</span><span class="sxs-lookup"><span data-stu-id="79443-129">Output</span></span>
- <span data-ttu-id="79443-130">Progresso</span><span class="sxs-lookup"><span data-stu-id="79443-130">Progress</span></span>
- <span data-ttu-id="79443-131">Detalha</span><span class="sxs-lookup"><span data-stu-id="79443-131">Verbose</span></span>
- <span data-ttu-id="79443-132">Avisa</span><span class="sxs-lookup"><span data-stu-id="79443-132">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79443-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79443-133">CommonParameters</span></span>
<span data-ttu-id="79443-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79443-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79443-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79443-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79443-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79443-136">INPUTS</span></span>

### <span data-ttu-id="79443-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="79443-137">None</span></span>
<span data-ttu-id="79443-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="79443-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79443-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79443-139">OUTPUTS</span></span>

### <span data-ttu-id="79443-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="79443-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="79443-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79443-141">NOTES</span></span>

## <span data-ttu-id="79443-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79443-142">RELATED LINKS</span></span>

[<span data-ttu-id="79443-143">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="79443-143">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="79443-144">Currículo-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="79443-144">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="79443-145">Parar-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="79443-145">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="79443-146">Suspender-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="79443-146">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


