---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 369dfd85b88b079e32e9ea65513d37c99f64b6fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893420"
---
# <span data-ttu-id="ec9ae-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="ec9ae-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="ec9ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9ae-103">Obtém a saída de um trabalho de sincronização de controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="ec9ae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ec9ae-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec9ae-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ec9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ec9ae-106">O cmdlet **Get-AzAutomationSourceControlSyncJobOutput** obtém a saída para um trabalho de sincronização de controle de origem de automação do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="ec9ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec9ae-107">EXAMPLES</span></span>

### <span data-ttu-id="ec9ae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec9ae-108">Example 1</span></span>
<span data-ttu-id="ec9ae-109">Este comando obtém a saída do trabalho de sincronização de controle de origem com a id 08d6d266-27b6-463c-beea-bc48a67ace15 para o controle de origem VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="ec9ae-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ec9ae-110">PARAMETERS</span></span>

### <span data-ttu-id="ec9ae-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ec9ae-111">-AutomationAccountName</span></span>
<span data-ttu-id="ec9ae-112">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-112">The automation account name.</span></span>

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

### <span data-ttu-id="ec9ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9ae-113">-DefaultProfile</span></span>
<span data-ttu-id="ec9ae-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec9ae-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="ec9ae-115">-JobId</span></span>
<span data-ttu-id="ec9ae-116">A ID do trabalho de sincronização do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec9ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec9ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec9ae-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-118">The resource group name.</span></span>

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

### <span data-ttu-id="ec9ae-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="ec9ae-119">-SourceControlName</span></span>
<span data-ttu-id="ec9ae-120">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-120">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec9ae-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="ec9ae-121">-Stream</span></span>
<span data-ttu-id="ec9ae-122">O tipo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-122">The stream type.</span></span>
<span data-ttu-id="ec9ae-123">O padrão é Any.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec9ae-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="ec9ae-124">-StreamId</span></span>
<span data-ttu-id="ec9ae-125">A ID do fluxo.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec9ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9ae-126">CommonParameters</span></span>
<span data-ttu-id="ec9ae-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec9ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9ae-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec9ae-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9ae-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec9ae-129">INPUTS</span></span>

### <span data-ttu-id="ec9ae-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ec9ae-130">System.String</span></span>

### <span data-ttu-id="ec9ae-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ec9ae-131">System.Guid</span></span>

### <span data-ttu-id="ec9ae-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="ec9ae-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="ec9ae-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ec9ae-133">OUTPUTS</span></span>

### <span data-ttu-id="ec9ae-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="ec9ae-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="ec9ae-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="ec9ae-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="ec9ae-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ec9ae-136">NOTES</span></span>

## <span data-ttu-id="ec9ae-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec9ae-137">RELATED LINKS</span></span>
