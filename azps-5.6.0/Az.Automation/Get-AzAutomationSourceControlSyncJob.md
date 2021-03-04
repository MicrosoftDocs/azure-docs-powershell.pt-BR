---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 76c2e4dd9de870ae9cdb8c5e26e96f80e477a3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893421"
---
# <span data-ttu-id="01a19-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="01a19-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="01a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01a19-102">SYNOPSIS</span></span>
<span data-ttu-id="01a19-103">Obtém trabalhos de sincronização de controle de origem da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="01a19-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="01a19-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="01a19-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01a19-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="01a19-105">DESCRIPTION</span></span>
<span data-ttu-id="01a19-106">O Get-AzAutomationSourceControlSyncJob cmdlet obtém trabalhos de sincronização de controle de origem do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="01a19-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="01a19-107">Para obter um trabalho de sincronização de controle de origem específico, especifique sua id.</span><span class="sxs-lookup"><span data-stu-id="01a19-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="01a19-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01a19-108">EXAMPLES</span></span>

### <span data-ttu-id="01a19-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01a19-109">Example 1</span></span>
<span data-ttu-id="01a19-110">Este comando obtém todos os trabalhos de sincronização de controle de origem de automação para o controle de origem VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="01a19-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="01a19-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="01a19-111">Example 2</span></span>
<span data-ttu-id="01a19-112">Este comando obtém o trabalho de sincronização de controle de origem com a id 08d6d266-27b6-463c-beea-bc48a67ace15 para o controle de origem VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="01a19-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative" `
                                                  -JobId "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

### <span data-ttu-id="01a19-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="01a19-113">Example 3</span></span>

<span data-ttu-id="01a19-114">Obtém trabalhos de sincronização de controle de origem da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="01a19-114">Gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="01a19-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="01a19-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAutomationSourceControlSyncJob -AutomationAccountName 'devAccount' -JobId 00000000-0000-0000-0000-00000000000000000 -ResourceGroupName 'rg1' -SourceControlName 'VSTSNative'
```

## <span data-ttu-id="01a19-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="01a19-116">PARAMETERS</span></span>

### <span data-ttu-id="01a19-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="01a19-117">-AutomationAccountName</span></span>
<span data-ttu-id="01a19-118">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="01a19-118">The automation account name.</span></span>

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

### <span data-ttu-id="01a19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a19-119">-DefaultProfile</span></span>
<span data-ttu-id="01a19-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01a19-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01a19-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="01a19-121">-JobId</span></span>
<span data-ttu-id="01a19-122">A ID do trabalho de sincronização do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="01a19-122">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01a19-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a19-123">-ResourceGroupName</span></span>
<span data-ttu-id="01a19-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="01a19-124">The resource group name.</span></span>

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

### <span data-ttu-id="01a19-125">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="01a19-125">-SourceControlName</span></span>
<span data-ttu-id="01a19-126">O nome de controle de origem do trabalho.</span><span class="sxs-lookup"><span data-stu-id="01a19-126">The source control name of the job.</span></span>

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

### <span data-ttu-id="01a19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a19-127">CommonParameters</span></span>
<span data-ttu-id="01a19-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01a19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a19-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a19-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a19-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01a19-130">INPUTS</span></span>

### <span data-ttu-id="01a19-131">System.String</span><span class="sxs-lookup"><span data-stu-id="01a19-131">System.String</span></span>

### <span data-ttu-id="01a19-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="01a19-132">System.Guid</span></span>

## <span data-ttu-id="01a19-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="01a19-133">OUTPUTS</span></span>

### <span data-ttu-id="01a19-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="01a19-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="01a19-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="01a19-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="01a19-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="01a19-136">NOTES</span></span>

## <span data-ttu-id="01a19-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01a19-137">RELATED LINKS</span></span>
