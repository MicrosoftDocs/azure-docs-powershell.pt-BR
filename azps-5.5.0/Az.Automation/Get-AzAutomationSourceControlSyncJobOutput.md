---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 6567d479ad0db7df959e4059155149f4fc06e1a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117004"
---
# <span data-ttu-id="fcfde-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="fcfde-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="fcfde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcfde-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfde-103">Obtém a saída de um trabalho de sincronização de controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcfde-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="fcfde-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcfde-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcfde-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fcfde-105">DESCRIPTION</span></span>
<span data-ttu-id="fcfde-106">O cmdlet **Get-AzAutomationSourceControlSync JobOutput** obtém a saída para um trabalho de sincronização de controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="fcfde-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="fcfde-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fcfde-107">EXAMPLES</span></span>

### <span data-ttu-id="fcfde-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fcfde-108">Example 1</span></span>
<span data-ttu-id="fcfde-109">Esse comando obtém a saída do trabalho de sincronização de controle de origem com a id 08d6d266-27b6-463c-beea-bc48a67ace15 para o controle de origem VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="fcfde-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


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

## <span data-ttu-id="fcfde-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcfde-110">PARAMETERS</span></span>

### <span data-ttu-id="fcfde-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fcfde-111">-AutomationAccountName</span></span>
<span data-ttu-id="fcfde-112">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="fcfde-112">The automation account name.</span></span>

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

### <span data-ttu-id="fcfde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfde-113">-DefaultProfile</span></span>
<span data-ttu-id="fcfde-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcfde-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcfde-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="fcfde-115">-JobId</span></span>
<span data-ttu-id="fcfde-116">A ID do trabalho de sincronização de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="fcfde-116">The source control sync job id.</span></span>

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

### <span data-ttu-id="fcfde-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcfde-117">-ResourceGroupName</span></span>
<span data-ttu-id="fcfde-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcfde-118">The resource group name.</span></span>

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

### <span data-ttu-id="fcfde-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="fcfde-119">-SourceControlName</span></span>
<span data-ttu-id="fcfde-120">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="fcfde-120">The source control name.</span></span>

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

### <span data-ttu-id="fcfde-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="fcfde-121">-Stream</span></span>
<span data-ttu-id="fcfde-122">O tipo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fcfde-122">The stream type.</span></span>
<span data-ttu-id="fcfde-123">Padrões para Qualquer.</span><span class="sxs-lookup"><span data-stu-id="fcfde-123">Defaults to Any.</span></span>

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

### <span data-ttu-id="fcfde-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="fcfde-124">-StreamId</span></span>
<span data-ttu-id="fcfde-125">A ID do fluxo.</span><span class="sxs-lookup"><span data-stu-id="fcfde-125">The stream id.</span></span>

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

### <span data-ttu-id="fcfde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfde-126">CommonParameters</span></span>
<span data-ttu-id="fcfde-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcfde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfde-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfde-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfde-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="fcfde-129">INPUTS</span></span>

### <span data-ttu-id="fcfde-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fcfde-130">System.String</span></span>

### <span data-ttu-id="fcfde-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="fcfde-131">System.Guid</span></span>

### <span data-ttu-id="fcfde-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncStreamType</span><span class="sxs-lookup"><span data-stu-id="fcfde-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="fcfde-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="fcfde-133">OUTPUTS</span></span>

### <span data-ttu-id="fcfde-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncStream</span><span class="sxs-lookup"><span data-stu-id="fcfde-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="fcfde-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncStreamRecord</span><span class="sxs-lookup"><span data-stu-id="fcfde-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="fcfde-136">Notas</span><span class="sxs-lookup"><span data-stu-id="fcfde-136">NOTES</span></span>

## <span data-ttu-id="fcfde-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcfde-137">RELATED LINKS</span></span>
