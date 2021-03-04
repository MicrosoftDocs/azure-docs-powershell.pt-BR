---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 89c1b96744ce67765bed53f850e21a457ead4b6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891233"
---
# <span data-ttu-id="7bc0c-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="7bc0c-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="7bc0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bc0c-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc0c-103">Obtém grupos de trabalho de runbook híbrido.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="7bc0c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7bc0c-104">SYNTAX</span></span>

### <span data-ttu-id="7bc0c-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7bc0c-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bc0c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7bc0c-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bc0c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bc0c-107">DESCRIPTION</span></span>
<span data-ttu-id="7bc0c-108">O cmdlet **Get-AzAutomationHybridWorkerGroup** obtém grupos de trabalho de runbook híbrido do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="7bc0c-109">Para obter um grupo específico, especifique seu nome.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="7bc0c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bc0c-110">EXAMPLES</span></span>

### <span data-ttu-id="7bc0c-111">Exemplo 1: Obter todos os grupos de trabalho de runbook híbrido</span><span class="sxs-lookup"><span data-stu-id="7bc0c-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7bc0c-112">Este comando obtém todos os grupos de trabalho de runbook híbrido na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7bc0c-113">Exemplo 2: Obter um único grupo de trabalho de runbook híbrido</span><span class="sxs-lookup"><span data-stu-id="7bc0c-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="7bc0c-114">Este comando obtém o grupo de trabalho de runbook híbrido chamado HybridRunbookWorkerGroup01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7bc0c-115">Exemplo 3: Obter os funcionários em um grupo de trabalho de runbook híbrido</span><span class="sxs-lookup"><span data-stu-id="7bc0c-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="7bc0c-116">Este comando obtém os funcionários de runbook híbrido no grupo de trabalho de runbook híbrido chamado HybridRunbookWorkerGroup01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7bc0c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7bc0c-117">PARAMETERS</span></span>

### <span data-ttu-id="7bc0c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7bc0c-118">-AutomationAccountName</span></span>
<span data-ttu-id="7bc0c-119">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="7bc0c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc0c-120">-DefaultProfile</span></span>
<span data-ttu-id="7bc0c-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7bc0c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bc0c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7bc0c-122">-Name</span></span>
<span data-ttu-id="7bc0c-123">Especifica o nome do grupo de trabalho de runbook híbrido.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc0c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc0c-124">-ResourceGroupName</span></span>
<span data-ttu-id="7bc0c-125">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7bc0c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc0c-126">CommonParameters</span></span>
<span data-ttu-id="7bc0c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc0c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc0c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc0c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc0c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bc0c-129">INPUTS</span></span>

### <span data-ttu-id="7bc0c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7bc0c-130">System.String</span></span>

## <span data-ttu-id="7bc0c-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7bc0c-131">OUTPUTS</span></span>

### <span data-ttu-id="7bc0c-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="7bc0c-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="7bc0c-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="7bc0c-133">NOTES</span></span>

## <span data-ttu-id="7bc0c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bc0c-134">RELATED LINKS</span></span>
