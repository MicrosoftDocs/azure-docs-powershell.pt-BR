---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942680"
---
# <span data-ttu-id="5d456-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="5d456-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="5d456-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d456-102">SYNOPSIS</span></span>
<span data-ttu-id="5d456-103">Obtém grupos de trabalhadores híbridos do runbook.</span><span class="sxs-lookup"><span data-stu-id="5d456-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="5d456-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d456-104">SYNTAX</span></span>

### <span data-ttu-id="5d456-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="5d456-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d456-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5d456-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d456-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d456-107">DESCRIPTION</span></span>
<span data-ttu-id="5d456-108">O cmdlet **Get-AzAutomationHybridWorkerGroup** Obtém grupos de trabalho do runbook híbrido do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5d456-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="5d456-109">Para obter um grupo específico, especifique o nome.</span><span class="sxs-lookup"><span data-stu-id="5d456-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="5d456-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d456-110">EXAMPLES</span></span>

### <span data-ttu-id="5d456-111">Exemplo 1: obter todos os grupos do Hybrid runbook Worker</span><span class="sxs-lookup"><span data-stu-id="5d456-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5d456-112">Esse comando obtém todos os grupos de Hybrid runbook Worker na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5d456-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5d456-113">Exemplo 2: obter um único grupo de operadores de runbook híbrido</span><span class="sxs-lookup"><span data-stu-id="5d456-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="5d456-114">Esse comando obtém o grupo do Hybrid runbook Worker chamado HybridRunbookWorkerGroup01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5d456-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5d456-115">Exemplo 3: obter os trabalhadores em um grupo de trabalho híbrido do runbook</span><span class="sxs-lookup"><span data-stu-id="5d456-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="5d456-116">Esse comando obtém os trabalhadores do runbook híbrido no grupo de trabalho híbrido do runbook chamado HybridRunbookWorkerGroup01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5d456-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5d456-117">OS</span><span class="sxs-lookup"><span data-stu-id="5d456-117">PARAMETERS</span></span>

### <span data-ttu-id="5d456-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5d456-118">-AutomationAccountName</span></span>
<span data-ttu-id="5d456-119">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="5d456-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="5d456-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d456-120">-DefaultProfile</span></span>
<span data-ttu-id="5d456-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5d456-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d456-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d456-122">-Name</span></span>
<span data-ttu-id="5d456-123">Especifica o nome do grupo do Hybrid runbook Worker.</span><span class="sxs-lookup"><span data-stu-id="5d456-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="5d456-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d456-124">-ResourceGroupName</span></span>
<span data-ttu-id="5d456-125">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d456-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5d456-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d456-126">CommonParameters</span></span>
<span data-ttu-id="5d456-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d456-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d456-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d456-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d456-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d456-129">INPUTS</span></span>

### <span data-ttu-id="5d456-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5d456-130">System.String</span></span>

## <span data-ttu-id="5d456-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d456-131">OUTPUTS</span></span>

### <span data-ttu-id="5d456-132">Microsoft. Azure. Commands. Automation. Model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="5d456-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="5d456-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d456-133">NOTES</span></span>

## <span data-ttu-id="5d456-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d456-134">RELATED LINKS</span></span>
