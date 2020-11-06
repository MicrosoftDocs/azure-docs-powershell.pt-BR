---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 4a5864e9572a21442a5333232fe5f705fb1b5687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426446"
---
# <span data-ttu-id="9d502-101">Start-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="9d502-101">Start-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="9d502-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d502-102">SYNOPSIS</span></span>
<span data-ttu-id="9d502-103">Inicia um trabalho de sincronização do controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="9d502-103">Starts an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d502-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d502-104">SYNTAX</span></span>

```
Start-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d502-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d502-105">DESCRIPTION</span></span>
<span data-ttu-id="9d502-106">O cmdlet Start-AzureRmAutomationSourceControlSyncJob inicia um trabalho de sincronização de controle de recurso de automação do Azure para o nome do controle do código-fonte fornecido.</span><span class="sxs-lookup"><span data-stu-id="9d502-106">The Start-AzureRmAutomationSourceControlSyncJob cmdlet starts a Azure Automation souce control sync job for the given source control name.</span></span>

## <span data-ttu-id="9d502-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d502-107">EXAMPLES</span></span>

### <span data-ttu-id="9d502-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9d502-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="9d502-109">OS</span><span class="sxs-lookup"><span data-stu-id="9d502-109">PARAMETERS</span></span>

### <span data-ttu-id="9d502-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d502-110">-AutomationAccountName</span></span>
<span data-ttu-id="9d502-111">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="9d502-111">The automation account name.</span></span>

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

### <span data-ttu-id="9d502-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d502-112">-DefaultProfile</span></span>
<span data-ttu-id="9d502-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d502-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d502-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="9d502-114">-JobId</span></span>
<span data-ttu-id="9d502-115">A ID do trabalho de sincronização do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="9d502-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d502-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d502-116">-ResourceGroupName</span></span>
<span data-ttu-id="9d502-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d502-117">The resource group name.</span></span>

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

### <span data-ttu-id="9d502-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="9d502-118">-SourceControlName</span></span>
<span data-ttu-id="9d502-119">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="9d502-119">The source control name.</span></span>

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

### <span data-ttu-id="9d502-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d502-120">-Confirm</span></span>
<span data-ttu-id="9d502-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d502-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d502-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d502-122">-WhatIf</span></span>
<span data-ttu-id="9d502-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d502-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d502-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d502-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d502-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d502-125">CommonParameters</span></span>
<span data-ttu-id="9d502-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d502-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d502-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d502-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d502-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d502-128">INPUTS</span></span>

### <span data-ttu-id="9d502-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9d502-129">System.String</span></span>

## <span data-ttu-id="9d502-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d502-130">OUTPUTS</span></span>

### <span data-ttu-id="9d502-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="9d502-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="9d502-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d502-132">NOTES</span></span>

## <span data-ttu-id="9d502-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d502-133">RELATED LINKS</span></span>
