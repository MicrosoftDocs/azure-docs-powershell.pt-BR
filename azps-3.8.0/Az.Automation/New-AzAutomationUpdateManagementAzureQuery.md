---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944953"
---
# <span data-ttu-id="4e345-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="4e345-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="4e345-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e345-102">SYNOPSIS</span></span>
<span data-ttu-id="4e345-103">Cria o objeto de consulta Azure de configuração da atualização do software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e345-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="4e345-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e345-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e345-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e345-105">DESCRIPTION</span></span>
<span data-ttu-id="4e345-106">Cria um objeto de consultas de configuração de atualização de software do Azure que será usado para criar uma configuração de atualização de software que será executada em um cronograma para atualizar uma lista de lista resolvida dinamicamente de máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e345-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="4e345-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e345-107">EXAMPLES</span></span>

### <span data-ttu-id="4e345-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e345-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="4e345-109">OS</span><span class="sxs-lookup"><span data-stu-id="4e345-109">PARAMETERS</span></span>

### <span data-ttu-id="4e345-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e345-110">-AutomationAccountName</span></span>
<span data-ttu-id="4e345-111">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="4e345-111">The automation account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e345-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e345-112">-DefaultProfile</span></span>
<span data-ttu-id="4e345-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e345-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e345-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="4e345-114">-FilterOperator</span></span>
<span data-ttu-id="4e345-115">Operador de filtro de marca.</span><span class="sxs-lookup"><span data-stu-id="4e345-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4e345-116">-Local</span><span class="sxs-lookup"><span data-stu-id="4e345-116">-Location</span></span>
<span data-ttu-id="4e345-117">Lista de locais para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e345-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4e345-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e345-118">-ResourceGroupName</span></span>
<span data-ttu-id="4e345-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4e345-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e345-120">-Escopo</span><span class="sxs-lookup"><span data-stu-id="4e345-120">-Scope</span></span>
<span data-ttu-id="4e345-121">IDs de recursos para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e345-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4e345-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="4e345-122">-Tag</span></span>
<span data-ttu-id="4e345-123">Marca para máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e345-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="4e345-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e345-124">CommonParameters</span></span>
<span data-ttu-id="4e345-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e345-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4e345-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e345-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e345-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e345-127">INPUTS</span></span>

### <span data-ttu-id="4e345-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="4e345-128">System.String[]</span></span>

### <span data-ttu-id="4e345-129">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4e345-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4e345-130">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. TagOperators</span><span class="sxs-lookup"><span data-stu-id="4e345-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="4e345-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4e345-131">System.String</span></span>

## <span data-ttu-id="4e345-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e345-132">OUTPUTS</span></span>

### <span data-ttu-id="4e345-133">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="4e345-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="4e345-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e345-134">NOTES</span></span>

## <span data-ttu-id="4e345-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e345-135">RELATED LINKS</span></span>
