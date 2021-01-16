---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432615"
---
# <span data-ttu-id="2adba-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="2adba-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="2adba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2adba-102">SYNOPSIS</span></span>
<span data-ttu-id="2adba-103">Obtém os fluxos de log de um trabalho de compilação DSC de automação.</span><span class="sxs-lookup"><span data-stu-id="2adba-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="2adba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2adba-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2adba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2adba-105">DESCRIPTION</span></span>
<span data-ttu-id="2adba-106">O cmdlet **Get-AzAutomationDscCompilationJobOutput** Obtém os registros de fluxo de um trabalho de compilação DSC (configuração de estado desejado APS) na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="2adba-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="2adba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2adba-107">EXAMPLES</span></span>

### <span data-ttu-id="2adba-108">Exemplo 1: obter os logs para um trabalho de compilação DSC</span><span class="sxs-lookup"><span data-stu-id="2adba-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="2adba-109">O primeiro comando obtém os trabalhos de compilação na conta de automação chamada Contoso17 usando o cmdlet Get-AzAutomationDscCompilationJob.</span><span class="sxs-lookup"><span data-stu-id="2adba-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="2adba-110">O comando armazena esses objetos na variável $Jobs.</span><span class="sxs-lookup"><span data-stu-id="2adba-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="2adba-111">O segundo comando obtém a saída do trabalho de compilação para qualquer fluxo para o primeiro membro da matriz de $Jobs.</span><span class="sxs-lookup"><span data-stu-id="2adba-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="2adba-112">OS</span><span class="sxs-lookup"><span data-stu-id="2adba-112">PARAMETERS</span></span>

### <span data-ttu-id="2adba-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2adba-113">-AutomationAccountName</span></span>
<span data-ttu-id="2adba-114">Especifica o nome da conta de automação que contém o trabalho de compilação DSC.</span><span class="sxs-lookup"><span data-stu-id="2adba-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="2adba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2adba-115">-DefaultProfile</span></span>
<span data-ttu-id="2adba-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2adba-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2adba-117">-ID</span><span class="sxs-lookup"><span data-stu-id="2adba-117">-Id</span></span>
<span data-ttu-id="2adba-118">Especifica a ID exclusiva do trabalho de compilação DSC para o qual esse cmdlet é apresentado.</span><span class="sxs-lookup"><span data-stu-id="2adba-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="2adba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2adba-119">-ResourceGroupName</span></span>
<span data-ttu-id="2adba-120">Especifica o nome do grupo de recursos que contém o trabalho de compilação DSC para o qual esse cmdlet obtém registros de fluxo.</span><span class="sxs-lookup"><span data-stu-id="2adba-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="2adba-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2adba-121">-StartTime</span></span>
<span data-ttu-id="2adba-122">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="2adba-122">Specifies a start time.</span></span>
<span data-ttu-id="2adba-123">Esse cmdlet obtém registros de fluxo que o trabalho de compilação DSC gera após esse tempo.</span><span class="sxs-lookup"><span data-stu-id="2adba-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="2adba-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="2adba-124">-Stream</span></span>
<span data-ttu-id="2adba-125">Especifica o tipo de fluxo para a saída obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2adba-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="2adba-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="2adba-126">Valid values are:</span></span> 
- <span data-ttu-id="2adba-127">Qualquer</span><span class="sxs-lookup"><span data-stu-id="2adba-127">Any</span></span> 
- <span data-ttu-id="2adba-128">Avisa</span><span class="sxs-lookup"><span data-stu-id="2adba-128">Warning</span></span> 
- <span data-ttu-id="2adba-129">Erros</span><span class="sxs-lookup"><span data-stu-id="2adba-129">Error</span></span> 
- <span data-ttu-id="2adba-130">Detalha</span><span class="sxs-lookup"><span data-stu-id="2adba-130">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2adba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2adba-131">CommonParameters</span></span>
<span data-ttu-id="2adba-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2adba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2adba-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2adba-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2adba-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2adba-134">INPUTS</span></span>

### <span data-ttu-id="2adba-135">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2adba-135">System.Guid</span></span>

### <span data-ttu-id="2adba-136">Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="2adba-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="2adba-137">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2adba-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2adba-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2adba-138">System.String</span></span>

## <span data-ttu-id="2adba-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2adba-139">OUTPUTS</span></span>

### <span data-ttu-id="2adba-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="2adba-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="2adba-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2adba-141">NOTES</span></span>

## <span data-ttu-id="2adba-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2adba-142">RELATED LINKS</span></span>

[<span data-ttu-id="2adba-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="2adba-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="2adba-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="2adba-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


