---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: a6d8a618ea9561c244b161407807ddfbe99b854a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117005"
---
# <span data-ttu-id="06563-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="06563-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="06563-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06563-102">SYNOPSIS</span></span>
<span data-ttu-id="06563-103">Obtém trabalhos de sincronização de controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="06563-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="06563-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06563-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06563-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="06563-105">DESCRIPTION</span></span>
<span data-ttu-id="06563-106">O Get-AzAutomationSourceControlSyncJob cmdlet obtém trabalhos de sincronização de controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="06563-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="06563-107">Para obter um trabalho de sincronização de controle de origem específico, especifique sua id.</span><span class="sxs-lookup"><span data-stu-id="06563-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="06563-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="06563-108">EXAMPLES</span></span>

### <span data-ttu-id="06563-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06563-109">Example 1</span></span>
<span data-ttu-id="06563-110">Esse comando obtém todos os trabalhos de sincronização de controle de origem de automação do VSTSNative do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="06563-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="06563-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="06563-111">Example 2</span></span>
<span data-ttu-id="06563-112">Esse comando obtém o trabalho de sincronização de controle de origem com a id 08d6d266-27b6-463c-beea-bc48a67ace15 para o controle de origem VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="06563-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative" `
                                                  -JobId "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

### <span data-ttu-id="06563-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="06563-113">Example 3</span></span>

<span data-ttu-id="06563-114">Obtém trabalhos de sincronização de controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="06563-114">Gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="06563-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="06563-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAutomationSourceControlSyncJob -AutomationAccountName 'devAccount' -JobId 00000000-0000-0000-0000-00000000000000000 -ResourceGroupName 'rg1' -SourceControlName 'VSTSNative'
```

## <span data-ttu-id="06563-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06563-116">PARAMETERS</span></span>

### <span data-ttu-id="06563-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="06563-117">-AutomationAccountName</span></span>
<span data-ttu-id="06563-118">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="06563-118">The automation account name.</span></span>

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

### <span data-ttu-id="06563-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06563-119">-DefaultProfile</span></span>
<span data-ttu-id="06563-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06563-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06563-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="06563-121">-JobId</span></span>
<span data-ttu-id="06563-122">A ID do trabalho de sincronização de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="06563-122">The source control sync job id.</span></span>

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

### <span data-ttu-id="06563-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06563-123">-ResourceGroupName</span></span>
<span data-ttu-id="06563-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06563-124">The resource group name.</span></span>

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

### <span data-ttu-id="06563-125">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="06563-125">-SourceControlName</span></span>
<span data-ttu-id="06563-126">O nome do controle de origem do trabalho.</span><span class="sxs-lookup"><span data-stu-id="06563-126">The source control name of the job.</span></span>

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

### <span data-ttu-id="06563-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06563-127">CommonParameters</span></span>
<span data-ttu-id="06563-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06563-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06563-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06563-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06563-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="06563-130">INPUTS</span></span>

### <span data-ttu-id="06563-131">System.String</span><span class="sxs-lookup"><span data-stu-id="06563-131">System.String</span></span>

### <span data-ttu-id="06563-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="06563-132">System.Guid</span></span>

## <span data-ttu-id="06563-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="06563-133">OUTPUTS</span></span>

### <span data-ttu-id="06563-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="06563-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="06563-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="06563-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="06563-136">Notas</span><span class="sxs-lookup"><span data-stu-id="06563-136">NOTES</span></span>

## <span data-ttu-id="06563-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06563-137">RELATED LINKS</span></span>
