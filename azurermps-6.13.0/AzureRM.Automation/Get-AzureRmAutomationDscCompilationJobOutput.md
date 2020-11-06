---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: a7ddc25fa7c6bc52acbe9369c569db060cf63a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426469"
---
# <span data-ttu-id="dc5c3-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="dc5c3-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="dc5c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5c3-103">Obtém os fluxos de log de um trabalho de compilação DSC de automação.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc5c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc5c3-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc5c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc5c3-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5c3-106">O cmdlet **Get-AzureRmAutomationDscCompilationJobOutput** Obtém os registros de fluxo de um trabalho de compilação DSC (configuração de estado desejado APS) na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="dc5c3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc5c3-107">EXAMPLES</span></span>

### <span data-ttu-id="dc5c3-108">Exemplo 1: obter os logs para um trabalho de compilação DSC</span><span class="sxs-lookup"><span data-stu-id="dc5c3-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="dc5c3-109">O primeiro comando obtém os trabalhos de compilação na conta de automação chamada Contoso17 usando o cmdlet Get-AzureRmAutomationDscCompilationJob.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="dc5c3-110">O comando armazena esses objetos na variável $Jobs.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="dc5c3-111">O segundo comando obtém a saída do trabalho de compilação para qualquer fluxo para o primeiro membro da matriz de $Jobs.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="dc5c3-112">OS</span><span class="sxs-lookup"><span data-stu-id="dc5c3-112">PARAMETERS</span></span>

### <span data-ttu-id="dc5c3-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dc5c3-113">-AutomationAccountName</span></span>
<span data-ttu-id="dc5c3-114">Especifica o nome da conta de automação que contém o trabalho de compilação DSC.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="dc5c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5c3-115">-DefaultProfile</span></span>
<span data-ttu-id="dc5c3-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dc5c3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5c3-117">-ID</span><span class="sxs-lookup"><span data-stu-id="dc5c3-117">-Id</span></span>
<span data-ttu-id="dc5c3-118">Especifica a ID exclusiva do trabalho de compilação DSC para o qual esse cmdlet é apresentado.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="dc5c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc5c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="dc5c3-120">Especifica o nome do grupo de recursos que contém o trabalho de compilação DSC para o qual esse cmdlet obtém registros de fluxo.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="dc5c3-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dc5c3-121">-StartTime</span></span>
<span data-ttu-id="dc5c3-122">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-122">Specifies a start time.</span></span>
<span data-ttu-id="dc5c3-123">Esse cmdlet obtém registros de fluxo que o trabalho de compilação DSC gera após esse tempo.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="dc5c3-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="dc5c3-124">-Stream</span></span>
<span data-ttu-id="dc5c3-125">Especifica o tipo de fluxo para a saída obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="dc5c3-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dc5c3-126">Valid values are:</span></span> 
- <span data-ttu-id="dc5c3-127">Qualquer</span><span class="sxs-lookup"><span data-stu-id="dc5c3-127">Any</span></span> 
- <span data-ttu-id="dc5c3-128">Avisa</span><span class="sxs-lookup"><span data-stu-id="dc5c3-128">Warning</span></span> 
- <span data-ttu-id="dc5c3-129">Erros</span><span class="sxs-lookup"><span data-stu-id="dc5c3-129">Error</span></span> 
- <span data-ttu-id="dc5c3-130">Detalha</span><span class="sxs-lookup"><span data-stu-id="dc5c3-130">Verbose</span></span>

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

### <span data-ttu-id="dc5c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5c3-131">CommonParameters</span></span>
<span data-ttu-id="dc5c3-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc5c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5c3-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5c3-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc5c3-134">INPUTS</span></span>

### <span data-ttu-id="dc5c3-135">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dc5c3-135">System.Guid</span></span>

### <span data-ttu-id="dc5c3-136">Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="dc5c3-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="dc5c3-137">System. Nullable ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dc5c3-137">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="dc5c3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dc5c3-138">System.String</span></span>

## <span data-ttu-id="dc5c3-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc5c3-139">OUTPUTS</span></span>

### <span data-ttu-id="dc5c3-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="dc5c3-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="dc5c3-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc5c3-141">NOTES</span></span>

## <span data-ttu-id="dc5c3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc5c3-142">RELATED LINKS</span></span>

[<span data-ttu-id="dc5c3-143">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="dc5c3-143">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="dc5c3-144">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="dc5c3-144">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


