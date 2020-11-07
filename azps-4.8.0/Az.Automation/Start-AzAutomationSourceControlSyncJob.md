---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955143"
---
# <span data-ttu-id="c9c80-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="c9c80-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="c9c80-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9c80-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c80-103">Inicia um trabalho de sincronização do controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c80-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="c9c80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9c80-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c80-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9c80-105">DESCRIPTION</span></span>
<span data-ttu-id="c9c80-106">O cmdlet Start-AzAutomationSourceControlSyncJob inicia um trabalho de sincronização do controle do código-fonte do Azure Automation para o nome do controle do código-fonte fornecido.</span><span class="sxs-lookup"><span data-stu-id="c9c80-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="c9c80-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9c80-107">EXAMPLES</span></span>

### <span data-ttu-id="c9c80-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9c80-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="c9c80-109">OS</span><span class="sxs-lookup"><span data-stu-id="c9c80-109">PARAMETERS</span></span>

### <span data-ttu-id="c9c80-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c9c80-110">-AutomationAccountName</span></span>
<span data-ttu-id="c9c80-111">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="c9c80-111">The automation account name.</span></span>

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

### <span data-ttu-id="c9c80-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c80-112">-DefaultProfile</span></span>
<span data-ttu-id="c9c80-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c80-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c80-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="c9c80-114">-JobId</span></span>
<span data-ttu-id="c9c80-115">A ID do trabalho de sincronização do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="c9c80-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="c9c80-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c80-116">-ResourceGroupName</span></span>
<span data-ttu-id="c9c80-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9c80-117">The resource group name.</span></span>

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

### <span data-ttu-id="c9c80-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="c9c80-118">-SourceControlName</span></span>
<span data-ttu-id="c9c80-119">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="c9c80-119">The source control name.</span></span>

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

### <span data-ttu-id="c9c80-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c9c80-120">-Confirm</span></span>
<span data-ttu-id="c9c80-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9c80-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c80-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c80-122">-WhatIf</span></span>
<span data-ttu-id="c9c80-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9c80-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c80-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9c80-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c80-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c80-125">CommonParameters</span></span>
<span data-ttu-id="c9c80-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c80-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c80-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c80-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c80-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9c80-128">INPUTS</span></span>

### <span data-ttu-id="c9c80-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c9c80-129">System.String</span></span>

## <span data-ttu-id="c9c80-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9c80-130">OUTPUTS</span></span>

### <span data-ttu-id="c9c80-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="c9c80-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="c9c80-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9c80-132">NOTES</span></span>

## <span data-ttu-id="c9c80-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9c80-133">RELATED LINKS</span></span>
