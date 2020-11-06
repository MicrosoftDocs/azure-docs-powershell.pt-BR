---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 63ff1ea82f3167738161191900e9516513b034bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597821"
---
# <span data-ttu-id="3bc96-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="3bc96-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="3bc96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3bc96-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc96-103">Obtém a saída de um trabalho de sincronização do controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc96-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="3bc96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3bc96-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3bc96-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc96-106">O cmdlet **Get-AzAutomationSourceControlSyncJobOutput** Obtém a saída de um trabalho de sincronização do controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc96-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="3bc96-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3bc96-107">EXAMPLES</span></span>

### <span data-ttu-id="3bc96-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3bc96-108">Example 1</span></span>
<span data-ttu-id="3bc96-109">Esse comando obtém a saída do trabalho de sincronização do controle do código-fonte com a ID 08d6d266-27b6-463c-beea-bc48a67ace15 para o VSTSNative de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="3bc96-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


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

## <span data-ttu-id="3bc96-110">OS</span><span class="sxs-lookup"><span data-stu-id="3bc96-110">PARAMETERS</span></span>

### <span data-ttu-id="3bc96-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3bc96-111">-AutomationAccountName</span></span>
<span data-ttu-id="3bc96-112">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="3bc96-112">The automation account name.</span></span>

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

### <span data-ttu-id="3bc96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc96-113">-DefaultProfile</span></span>
<span data-ttu-id="3bc96-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc96-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="3bc96-115">-JobId</span></span>
<span data-ttu-id="3bc96-116">A ID do trabalho de sincronização do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="3bc96-116">The source control sync job id.</span></span>

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

### <span data-ttu-id="3bc96-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc96-117">-ResourceGroupName</span></span>
<span data-ttu-id="3bc96-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3bc96-118">The resource group name.</span></span>

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

### <span data-ttu-id="3bc96-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="3bc96-119">-SourceControlName</span></span>
<span data-ttu-id="3bc96-120">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="3bc96-120">The source control name.</span></span>

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

### <span data-ttu-id="3bc96-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="3bc96-121">-Stream</span></span>
<span data-ttu-id="3bc96-122">O tipo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="3bc96-122">The stream type.</span></span>
<span data-ttu-id="3bc96-123">O padrão é qualquer.</span><span class="sxs-lookup"><span data-stu-id="3bc96-123">Defaults to Any.</span></span>

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

### <span data-ttu-id="3bc96-124">-Streamid</span><span class="sxs-lookup"><span data-stu-id="3bc96-124">-StreamId</span></span>
<span data-ttu-id="3bc96-125">A ID do fluxo.</span><span class="sxs-lookup"><span data-stu-id="3bc96-125">The stream id.</span></span>

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

### <span data-ttu-id="3bc96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc96-126">CommonParameters</span></span>
<span data-ttu-id="3bc96-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc96-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc96-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc96-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3bc96-129">INPUTS</span></span>

### <span data-ttu-id="3bc96-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc96-130">System.String</span></span>

### <span data-ttu-id="3bc96-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3bc96-131">System.Guid</span></span>

### <span data-ttu-id="3bc96-132">Microsoft. Azure. Commands. Automation. Common. SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="3bc96-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="3bc96-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3bc96-133">OUTPUTS</span></span>

### <span data-ttu-id="3bc96-134">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="3bc96-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="3bc96-135">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="3bc96-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="3bc96-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3bc96-136">NOTES</span></span>

## <span data-ttu-id="3bc96-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3bc96-137">RELATED LINKS</span></span>
