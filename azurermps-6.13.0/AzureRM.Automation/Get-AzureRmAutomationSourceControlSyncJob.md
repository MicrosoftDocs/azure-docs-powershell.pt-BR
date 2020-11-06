---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 213df264e4ecd458c8505d521556f49265577333
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432807"
---
# <span data-ttu-id="28de6-101">Get-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="28de6-101">Get-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="28de6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28de6-102">SYNOPSIS</span></span>
<span data-ttu-id="28de6-103">Obtém trabalhos de sincronização do controle de origem da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="28de6-103">Gets Azure Automation source control sync jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28de6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28de6-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28de6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28de6-105">DESCRIPTION</span></span>
<span data-ttu-id="28de6-106">O cmdlet Get-AzureRmAutomationSourceControlSyncJob Obtém trabalhos de sincronização do controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="28de6-106">The Get-AzureRmAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="28de6-107">Para obter um trabalho de sincronização específico do controle do código-fonte, especifique sua ID.</span><span class="sxs-lookup"><span data-stu-id="28de6-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="28de6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28de6-108">EXAMPLES</span></span>

### <span data-ttu-id="28de6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28de6-109">Example 1</span></span>
<span data-ttu-id="28de6-110">Esse comando obtém todos os trabalhos de sincronização do controle de origem de automação para o VSTSNative de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="28de6-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="28de6-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28de6-111">Example 2</span></span>
<span data-ttu-id="28de6-112">Este comando obtém o trabalho de sincronização do controle do código-fonte com a ID 08d6d266-27b6-463c-beea-bc48a67ace15 para o VSTSNative de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="28de6-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="28de6-113">OS</span><span class="sxs-lookup"><span data-stu-id="28de6-113">PARAMETERS</span></span>

### <span data-ttu-id="28de6-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="28de6-114">-AutomationAccountName</span></span>
<span data-ttu-id="28de6-115">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="28de6-115">The automation account name.</span></span>

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

### <span data-ttu-id="28de6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28de6-116">-DefaultProfile</span></span>
<span data-ttu-id="28de6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28de6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28de6-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="28de6-118">-JobId</span></span>
<span data-ttu-id="28de6-119">A ID do trabalho de sincronização do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="28de6-119">The source control sync job id.</span></span>

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

### <span data-ttu-id="28de6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28de6-120">-ResourceGroupName</span></span>
<span data-ttu-id="28de6-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="28de6-121">The resource group name.</span></span>

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

### <span data-ttu-id="28de6-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="28de6-122">-SourceControlName</span></span>
<span data-ttu-id="28de6-123">O nome do controle de origem do trabalho.</span><span class="sxs-lookup"><span data-stu-id="28de6-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="28de6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28de6-124">CommonParameters</span></span>
<span data-ttu-id="28de6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28de6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28de6-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28de6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28de6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28de6-127">INPUTS</span></span>

### <span data-ttu-id="28de6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="28de6-128">System.String</span></span>

### <span data-ttu-id="28de6-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="28de6-129">System.Guid</span></span>

## <span data-ttu-id="28de6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28de6-130">OUTPUTS</span></span>

### <span data-ttu-id="28de6-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="28de6-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="28de6-132">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="28de6-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="28de6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28de6-133">NOTES</span></span>

## <span data-ttu-id="28de6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28de6-134">RELATED LINKS</span></span>
