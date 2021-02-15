---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112238"
---
# <span data-ttu-id="b479d-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="b479d-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="b479d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b479d-102">SYNOPSIS</span></span>
<span data-ttu-id="b479d-103">Inicia um trabalho de sincronização de controle de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="b479d-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="b479d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b479d-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b479d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b479d-105">DESCRIPTION</span></span>
<span data-ttu-id="b479d-106">O Start-AzAutomationSourceControlSyncJob cmdlet inicia um trabalho de sincronização de controle de origem de automação do Azure para o nome de controle de origem determinado.</span><span class="sxs-lookup"><span data-stu-id="b479d-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="b479d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b479d-107">EXAMPLES</span></span>

### <span data-ttu-id="b479d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b479d-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="b479d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b479d-109">PARAMETERS</span></span>

### <span data-ttu-id="b479d-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b479d-110">-AutomationAccountName</span></span>
<span data-ttu-id="b479d-111">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="b479d-111">The automation account name.</span></span>

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

### <span data-ttu-id="b479d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b479d-112">-DefaultProfile</span></span>
<span data-ttu-id="b479d-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b479d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b479d-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="b479d-114">-JobId</span></span>
<span data-ttu-id="b479d-115">A ID do trabalho de sincronização de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="b479d-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="b479d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b479d-116">-ResourceGroupName</span></span>
<span data-ttu-id="b479d-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b479d-117">The resource group name.</span></span>

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

### <span data-ttu-id="b479d-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="b479d-118">-SourceControlName</span></span>
<span data-ttu-id="b479d-119">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="b479d-119">The source control name.</span></span>

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

### <span data-ttu-id="b479d-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b479d-120">-Confirm</span></span>
<span data-ttu-id="b479d-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b479d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b479d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b479d-122">-WhatIf</span></span>
<span data-ttu-id="b479d-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b479d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b479d-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b479d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b479d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b479d-125">CommonParameters</span></span>
<span data-ttu-id="b479d-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b479d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b479d-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b479d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b479d-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="b479d-128">INPUTS</span></span>

### <span data-ttu-id="b479d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b479d-129">System.String</span></span>

## <span data-ttu-id="b479d-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="b479d-130">OUTPUTS</span></span>

### <span data-ttu-id="b479d-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="b479d-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="b479d-132">Notas</span><span class="sxs-lookup"><span data-stu-id="b479d-132">NOTES</span></span>

## <span data-ttu-id="b479d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b479d-133">RELATED LINKS</span></span>
