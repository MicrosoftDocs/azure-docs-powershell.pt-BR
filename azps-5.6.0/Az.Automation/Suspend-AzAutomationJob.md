---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 035cd77ab389b9c3cdce686620b3157b4b046c41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889045"
---
# <span data-ttu-id="edb60-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="edb60-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="edb60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb60-102">SYNOPSIS</span></span>
<span data-ttu-id="edb60-103">Suspende um trabalho de Automação.</span><span class="sxs-lookup"><span data-stu-id="edb60-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="edb60-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="edb60-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edb60-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="edb60-105">DESCRIPTION</span></span>
<span data-ttu-id="edb60-106">O cmdlet **Suspend-AzAutomationJob** suspende um trabalho de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="edb60-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="edb60-107">Especifique um trabalho de Automação em execução.</span><span class="sxs-lookup"><span data-stu-id="edb60-107">Specify a running Automation job.</span></span>
<span data-ttu-id="edb60-108">Para retomar um trabalho suspenso, use o Resume-AzAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb60-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="edb60-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edb60-109">EXAMPLES</span></span>

### <span data-ttu-id="edb60-110">Exemplo 1: Suspender um trabalho</span><span class="sxs-lookup"><span data-stu-id="edb60-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="edb60-111">Este comando suspende o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="edb60-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="edb60-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="edb60-112">PARAMETERS</span></span>

### <span data-ttu-id="edb60-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="edb60-113">-AutomationAccountName</span></span>
<span data-ttu-id="edb60-114">Especifica o nome de uma conta de Automação na qual esse cmdlet suspende um trabalho.</span><span class="sxs-lookup"><span data-stu-id="edb60-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="edb60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb60-115">-DefaultProfile</span></span>
<span data-ttu-id="edb60-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="edb60-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edb60-117">-Id</span><span class="sxs-lookup"><span data-stu-id="edb60-117">-Id</span></span>
<span data-ttu-id="edb60-118">Especifica a ID de um trabalho que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="edb60-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="edb60-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb60-119">-ResourceGroupName</span></span>
<span data-ttu-id="edb60-120">Especifica a ID de um trabalho que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="edb60-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="edb60-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb60-121">CommonParameters</span></span>
<span data-ttu-id="edb60-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb60-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb60-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb60-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb60-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edb60-124">INPUTS</span></span>

### <span data-ttu-id="edb60-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="edb60-125">System.Guid</span></span>

### <span data-ttu-id="edb60-126">System.String</span><span class="sxs-lookup"><span data-stu-id="edb60-126">System.String</span></span>

## <span data-ttu-id="edb60-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="edb60-127">OUTPUTS</span></span>

### <span data-ttu-id="edb60-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="edb60-128">System.Void</span></span>

## <span data-ttu-id="edb60-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="edb60-129">NOTES</span></span>

## <span data-ttu-id="edb60-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edb60-130">RELATED LINKS</span></span>

[<span data-ttu-id="edb60-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="edb60-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="edb60-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="edb60-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="edb60-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="edb60-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="edb60-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="edb60-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


