---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116828"
---
# <span data-ttu-id="899f7-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="899f7-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="899f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="899f7-102">SYNOPSIS</span></span>
<span data-ttu-id="899f7-103">Remove um runbook.</span><span class="sxs-lookup"><span data-stu-id="899f7-103">Removes a runbook.</span></span>

## <span data-ttu-id="899f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="899f7-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="899f7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="899f7-105">DESCRIPTION</span></span>
<span data-ttu-id="899f7-106">O cmdlet **Remove-AzAutomationRunbook** remove um runbook da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="899f7-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="899f7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="899f7-107">EXAMPLES</span></span>

### <span data-ttu-id="899f7-108">Exemplo 1: remover um runbook</span><span class="sxs-lookup"><span data-stu-id="899f7-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="899f7-109">Esse comando Remove o runbook chamado Runbook03 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="899f7-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="899f7-110">OS</span><span class="sxs-lookup"><span data-stu-id="899f7-110">PARAMETERS</span></span>

### <span data-ttu-id="899f7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="899f7-111">-AutomationAccountName</span></span>
<span data-ttu-id="899f7-112">Especifica o nome da conta de automação na qual esse cmdlet Remove um runbook.</span><span class="sxs-lookup"><span data-stu-id="899f7-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="899f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899f7-113">-DefaultProfile</span></span>
<span data-ttu-id="899f7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="899f7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="899f7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="899f7-115">-Force</span></span>
<span data-ttu-id="899f7-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="899f7-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899f7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="899f7-117">-Name</span></span>
<span data-ttu-id="899f7-118">Especifica o nome do runbook que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="899f7-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="899f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="899f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="899f7-120">Especifica o nome do grupo de recursos para o qual esse cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="899f7-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="899f7-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="899f7-121">-Confirm</span></span>
<span data-ttu-id="899f7-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="899f7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="899f7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="899f7-123">-WhatIf</span></span>
<span data-ttu-id="899f7-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="899f7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="899f7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="899f7-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899f7-126">CommonParameters</span></span>
<span data-ttu-id="899f7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="899f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899f7-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="899f7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899f7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="899f7-129">INPUTS</span></span>

### <span data-ttu-id="899f7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="899f7-130">System.String</span></span>

## <span data-ttu-id="899f7-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="899f7-131">OUTPUTS</span></span>

### <span data-ttu-id="899f7-132">System. void</span><span class="sxs-lookup"><span data-stu-id="899f7-132">System.Void</span></span>

## <span data-ttu-id="899f7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="899f7-133">NOTES</span></span>

## <span data-ttu-id="899f7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="899f7-134">RELATED LINKS</span></span>

[<span data-ttu-id="899f7-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="899f7-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="899f7-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="899f7-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="899f7-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="899f7-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="899f7-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="899f7-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="899f7-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="899f7-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="899f7-140">Publicar-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="899f7-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="899f7-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="899f7-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="899f7-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="899f7-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


