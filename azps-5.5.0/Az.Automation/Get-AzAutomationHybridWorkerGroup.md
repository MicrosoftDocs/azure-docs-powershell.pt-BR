---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112259"
---
# <span data-ttu-id="60866-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="60866-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="60866-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60866-102">SYNOPSIS</span></span>
<span data-ttu-id="60866-103">Obtém grupos de trabalhadores de runbook híbridos.</span><span class="sxs-lookup"><span data-stu-id="60866-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="60866-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60866-104">SYNTAX</span></span>

### <span data-ttu-id="60866-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="60866-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60866-106">ByName</span><span class="sxs-lookup"><span data-stu-id="60866-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60866-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="60866-107">DESCRIPTION</span></span>
<span data-ttu-id="60866-108">O cmdlet **Get-AzAutomationHybridWorkerGroup** obtém grupos de trabalhadores híbridos do runbook Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="60866-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="60866-109">Para obter um grupo específico, especifique seu nome.</span><span class="sxs-lookup"><span data-stu-id="60866-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="60866-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="60866-110">EXAMPLES</span></span>

### <span data-ttu-id="60866-111">Exemplo 1: Obter todos os grupos de trabalhadores de runbook híbridos</span><span class="sxs-lookup"><span data-stu-id="60866-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="60866-112">Esse comando obtém todos os grupos de trabalhadores de runbook híbridos na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="60866-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="60866-113">Exemplo 2: Obter um único grupo de trabalhadores de runbook híbrido</span><span class="sxs-lookup"><span data-stu-id="60866-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="60866-114">Esse comando obtém o grupo de trabalhadores de runbook híbrido chamado HybridRunbookWorkerGroup01 na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="60866-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="60866-115">Exemplo 3: Obter os trabalhadores em um grupo de trabalhadores de um runbook híbrido</span><span class="sxs-lookup"><span data-stu-id="60866-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="60866-116">Esse comando obtém os trabalhadores de um runbook híbrido no grupo de trabalhadores de runbook híbrido chamado HybridRunbookWorkerGroup01 na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="60866-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="60866-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60866-117">PARAMETERS</span></span>

### <span data-ttu-id="60866-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60866-118">-AutomationAccountName</span></span>
<span data-ttu-id="60866-119">Especifica o nome de uma conta de Automação.</span><span class="sxs-lookup"><span data-stu-id="60866-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="60866-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60866-120">-DefaultProfile</span></span>
<span data-ttu-id="60866-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="60866-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60866-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="60866-122">-Name</span></span>
<span data-ttu-id="60866-123">Especifica o nome do grupo de trabalhadores de runbook híbrido.</span><span class="sxs-lookup"><span data-stu-id="60866-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="60866-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60866-124">-ResourceGroupName</span></span>
<span data-ttu-id="60866-125">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60866-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="60866-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60866-126">CommonParameters</span></span>
<span data-ttu-id="60866-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60866-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60866-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60866-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60866-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="60866-129">INPUTS</span></span>

### <span data-ttu-id="60866-130">System.String</span><span class="sxs-lookup"><span data-stu-id="60866-130">System.String</span></span>

## <span data-ttu-id="60866-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="60866-131">OUTPUTS</span></span>

### <span data-ttu-id="60866-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="60866-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="60866-133">Notas</span><span class="sxs-lookup"><span data-stu-id="60866-133">NOTES</span></span>

## <span data-ttu-id="60866-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60866-134">RELATED LINKS</span></span>
