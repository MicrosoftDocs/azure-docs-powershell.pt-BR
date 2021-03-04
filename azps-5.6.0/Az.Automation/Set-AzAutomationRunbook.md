---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 26a84b381e3193f9f95f21135f40489f0cacb754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892242"
---
# <span data-ttu-id="abe1e-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="abe1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abe1e-102">SYNOPSIS</span></span>
<span data-ttu-id="abe1e-103">Modifica um runbook.</span><span class="sxs-lookup"><span data-stu-id="abe1e-103">Modifies a runbook.</span></span>

## <span data-ttu-id="abe1e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="abe1e-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abe1e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="abe1e-105">DESCRIPTION</span></span>
<span data-ttu-id="abe1e-106">O cmdlet **Set-AzAutomationRunbook** modifica a configuração de um runbook de Automação do Azure no APS.</span><span class="sxs-lookup"><span data-stu-id="abe1e-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="abe1e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abe1e-107">EXAMPLES</span></span>

### <span data-ttu-id="abe1e-108">Exemplo 1: Habilitar o log detalhado para um runbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="abe1e-109">Este comando habilita o log detalhado para os trabalhos do runbook especificado na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="abe1e-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="abe1e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="abe1e-110">PARAMETERS</span></span>

### <span data-ttu-id="abe1e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="abe1e-111">-AutomationAccountName</span></span>
<span data-ttu-id="abe1e-112">Especifica o nome da conta de automação na qual este cmdlet modifica um runbook.</span><span class="sxs-lookup"><span data-stu-id="abe1e-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="abe1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe1e-113">-DefaultProfile</span></span>
<span data-ttu-id="abe1e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="abe1e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abe1e-115">-Description</span><span class="sxs-lookup"><span data-stu-id="abe1e-115">-Description</span></span>
<span data-ttu-id="abe1e-116">Especifica uma descrição para o runbook.</span><span class="sxs-lookup"><span data-stu-id="abe1e-116">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe1e-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="abe1e-117">-LogProgress</span></span>
<span data-ttu-id="abe1e-118">Especifica se o runbook registra o andamento.</span><span class="sxs-lookup"><span data-stu-id="abe1e-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe1e-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="abe1e-119">-LogVerbose</span></span>
<span data-ttu-id="abe1e-120">Especifica se o registro em log inclui informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="abe1e-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe1e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="abe1e-121">-Name</span></span>
<span data-ttu-id="abe1e-122">Especifica o nome do runbook que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="abe1e-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe1e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abe1e-123">-ResourceGroupName</span></span>
<span data-ttu-id="abe1e-124">Especifica o nome do grupo de recursos para o qual este cmdlet modifica um runbook.</span><span class="sxs-lookup"><span data-stu-id="abe1e-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="abe1e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="abe1e-125">-Tag</span></span>
<span data-ttu-id="abe1e-126">As marcas do runbook.</span><span class="sxs-lookup"><span data-stu-id="abe1e-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abe1e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe1e-127">CommonParameters</span></span>
<span data-ttu-id="abe1e-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abe1e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe1e-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abe1e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe1e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="abe1e-130">INPUTS</span></span>

### <span data-ttu-id="abe1e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="abe1e-131">System.String</span></span>

### <span data-ttu-id="abe1e-132">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="abe1e-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="abe1e-133">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="abe1e-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="abe1e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="abe1e-134">OUTPUTS</span></span>

### <span data-ttu-id="abe1e-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="abe1e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="abe1e-136">NOTES</span></span>

## <span data-ttu-id="abe1e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abe1e-137">RELATED LINKS</span></span>

[<span data-ttu-id="abe1e-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="abe1e-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="abe1e-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="abe1e-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="abe1e-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="abe1e-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="abe1e-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="abe1e-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="abe1e-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


