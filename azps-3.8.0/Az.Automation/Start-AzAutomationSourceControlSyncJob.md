---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940569"
---
# <span data-ttu-id="1d0c1-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="1d0c1-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="1d0c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d0c1-102">SYNOPSIS</span></span>
<span data-ttu-id="1d0c1-103">Inicia um trabalho de sincronização do controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="1d0c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d0c1-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d0c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d0c1-105">DESCRIPTION</span></span>
<span data-ttu-id="1d0c1-106">O cmdlet Start-AzAutomationSourceControlSyncJob inicia um trabalho de sincronização do controle do código-fonte do Azure Automation para o nome do controle do código-fonte fornecido.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="1d0c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d0c1-107">EXAMPLES</span></span>

### <span data-ttu-id="1d0c1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d0c1-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="1d0c1-109">OS</span><span class="sxs-lookup"><span data-stu-id="1d0c1-109">PARAMETERS</span></span>

### <span data-ttu-id="1d0c1-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d0c1-110">-AutomationAccountName</span></span>
<span data-ttu-id="1d0c1-111">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-111">The automation account name.</span></span>

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

### <span data-ttu-id="1d0c1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d0c1-112">-DefaultProfile</span></span>
<span data-ttu-id="1d0c1-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d0c1-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="1d0c1-114">-JobId</span></span>
<span data-ttu-id="1d0c1-115">A ID do trabalho de sincronização do controle do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="1d0c1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d0c1-116">-ResourceGroupName</span></span>
<span data-ttu-id="1d0c1-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-117">The resource group name.</span></span>

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

### <span data-ttu-id="1d0c1-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="1d0c1-118">-SourceControlName</span></span>
<span data-ttu-id="1d0c1-119">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-119">The source control name.</span></span>

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

### <span data-ttu-id="1d0c1-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1d0c1-120">-Confirm</span></span>
<span data-ttu-id="1d0c1-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d0c1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d0c1-122">-WhatIf</span></span>
<span data-ttu-id="1d0c1-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d0c1-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d0c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d0c1-125">CommonParameters</span></span>
<span data-ttu-id="1d0c1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d0c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d0c1-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d0c1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d0c1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d0c1-128">INPUTS</span></span>

### <span data-ttu-id="1d0c1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1d0c1-129">System.String</span></span>

## <span data-ttu-id="1d0c1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d0c1-130">OUTPUTS</span></span>

### <span data-ttu-id="1d0c1-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="1d0c1-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="1d0c1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d0c1-132">NOTES</span></span>

## <span data-ttu-id="1d0c1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d0c1-133">RELATED LINKS</span></span>
