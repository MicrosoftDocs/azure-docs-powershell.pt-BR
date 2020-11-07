---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 5284f2ae8825f801e18752e21a5fe9b8cf43ac32
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944993"
---
# <span data-ttu-id="baa59-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="baa59-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="baa59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="baa59-102">SYNOPSIS</span></span>
<span data-ttu-id="baa59-103">Obtém trabalhos de sincronização do controle de origem da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="baa59-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="baa59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="baa59-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baa59-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="baa59-105">DESCRIPTION</span></span>
<span data-ttu-id="baa59-106">O cmdlet Get-AzAutomationSourceControlSyncJob Obtém trabalhos de sincronização do controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="baa59-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="baa59-107">Para obter um trabalho de sincronização específico do controle do código-fonte, especifique sua ID.</span><span class="sxs-lookup"><span data-stu-id="baa59-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="baa59-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="baa59-108">EXAMPLES</span></span>

### <span data-ttu-id="baa59-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="baa59-109">Example 1</span></span>
<span data-ttu-id="baa59-110">Esse comando obtém todos os trabalhos de sincronização do controle de origem de automação para o VSTSNative de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="baa59-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="baa59-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="baa59-111">Example 2</span></span>
<span data-ttu-id="baa59-112">Este comando obtém o trabalho de sincronização do controle do código-fonte com a ID 08d6d266-27b6-463c-beea-bc48a67ace15 para o VSTSNative de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="baa59-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="baa59-113">OS</span><span class="sxs-lookup"><span data-stu-id="baa59-113">PARAMETERS</span></span>

### <span data-ttu-id="baa59-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="baa59-114">-AutomationAccountName</span></span>
<span data-ttu-id="baa59-115">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="baa59-115">The automation account name.</span></span>

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

### <span data-ttu-id="baa59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa59-116">-DefaultProfile</span></span>
<span data-ttu-id="baa59-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="baa59-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baa59-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="baa59-118">-JobId</span></span>
<span data-ttu-id="baa59-119">A ID do trabalho de sincronização do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="baa59-119">The source control sync job id.</span></span>

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

### <span data-ttu-id="baa59-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa59-120">-ResourceGroupName</span></span>
<span data-ttu-id="baa59-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="baa59-121">The resource group name.</span></span>

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

### <span data-ttu-id="baa59-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="baa59-122">-SourceControlName</span></span>
<span data-ttu-id="baa59-123">O nome do controle de origem do trabalho.</span><span class="sxs-lookup"><span data-stu-id="baa59-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="baa59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa59-124">CommonParameters</span></span>
<span data-ttu-id="baa59-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baa59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa59-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa59-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa59-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="baa59-127">INPUTS</span></span>

### <span data-ttu-id="baa59-128">System. String</span><span class="sxs-lookup"><span data-stu-id="baa59-128">System.String</span></span>

### <span data-ttu-id="baa59-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="baa59-129">System.Guid</span></span>

## <span data-ttu-id="baa59-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="baa59-130">OUTPUTS</span></span>

### <span data-ttu-id="baa59-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="baa59-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="baa59-132">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="baa59-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="baa59-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="baa59-133">NOTES</span></span>

## <span data-ttu-id="baa59-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baa59-134">RELATED LINKS</span></span>
