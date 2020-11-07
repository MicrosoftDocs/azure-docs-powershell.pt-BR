---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 6567d479ad0db7df959e4059155149f4fc06e1a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944992"
---
# <span data-ttu-id="f32f4-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="f32f4-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="f32f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f32f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f32f4-103">Obtém a saída de um trabalho de sincronização do controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="f32f4-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="f32f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f32f4-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f32f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f32f4-105">DESCRIPTION</span></span>
<span data-ttu-id="f32f4-106">O cmdlet **Get-AzAutomationSourceControlSyncJobOutput** Obtém a saída de um trabalho de sincronização do controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="f32f4-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="f32f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f32f4-107">EXAMPLES</span></span>

### <span data-ttu-id="f32f4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f32f4-108">Example 1</span></span>
<span data-ttu-id="f32f4-109">Esse comando obtém a saída do trabalho de sincronização do controle do código-fonte com a ID 08d6d266-27b6-463c-beea-bc48a67ace15 para o VSTSNative de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="f32f4-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


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

## <span data-ttu-id="f32f4-110">OS</span><span class="sxs-lookup"><span data-stu-id="f32f4-110">PARAMETERS</span></span>

### <span data-ttu-id="f32f4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f32f4-111">-AutomationAccountName</span></span>
<span data-ttu-id="f32f4-112">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="f32f4-112">The automation account name.</span></span>

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

### <span data-ttu-id="f32f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f32f4-113">-DefaultProfile</span></span>
<span data-ttu-id="f32f4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f32f4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f32f4-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="f32f4-115">-JobId</span></span>
<span data-ttu-id="f32f4-116">A ID do trabalho de sincronização do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="f32f4-116">The source control sync job id.</span></span>

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

### <span data-ttu-id="f32f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f32f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="f32f4-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f32f4-118">The resource group name.</span></span>

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

### <span data-ttu-id="f32f4-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="f32f4-119">-SourceControlName</span></span>
<span data-ttu-id="f32f4-120">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="f32f4-120">The source control name.</span></span>

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

### <span data-ttu-id="f32f4-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="f32f4-121">-Stream</span></span>
<span data-ttu-id="f32f4-122">O tipo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f32f4-122">The stream type.</span></span>
<span data-ttu-id="f32f4-123">O padrão é qualquer.</span><span class="sxs-lookup"><span data-stu-id="f32f4-123">Defaults to Any.</span></span>

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

### <span data-ttu-id="f32f4-124">-Streamid</span><span class="sxs-lookup"><span data-stu-id="f32f4-124">-StreamId</span></span>
<span data-ttu-id="f32f4-125">A ID do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f32f4-125">The stream id.</span></span>

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

### <span data-ttu-id="f32f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32f4-126">CommonParameters</span></span>
<span data-ttu-id="f32f4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f32f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32f4-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f32f4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32f4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f32f4-129">INPUTS</span></span>

### <span data-ttu-id="f32f4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f32f4-130">System.String</span></span>

### <span data-ttu-id="f32f4-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f32f4-131">System.Guid</span></span>

### <span data-ttu-id="f32f4-132">Microsoft. Azure. Commands. Automation. Common. SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="f32f4-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="f32f4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f32f4-133">OUTPUTS</span></span>

### <span data-ttu-id="f32f4-134">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="f32f4-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="f32f4-135">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="f32f4-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="f32f4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f32f4-136">NOTES</span></span>

## <span data-ttu-id="f32f4-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f32f4-137">RELATED LINKS</span></span>
