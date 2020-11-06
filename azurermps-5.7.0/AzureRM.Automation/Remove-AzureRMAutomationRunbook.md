---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: a4f65e20253ef979cba5d3907faeba3fb58e7fe6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440878"
---
# <span data-ttu-id="c3e75-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="c3e75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3e75-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e75-103">Remove um runbook.</span><span class="sxs-lookup"><span data-stu-id="c3e75-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3e75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3e75-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3e75-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3e75-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e75-106">O cmdlet **Remove-AzureRmAutomationRunbook** remove um runbook da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e75-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="c3e75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3e75-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e75-108">Exemplo 1: remover um runbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c3e75-109">Esse comando Remove o runbook chamado Runbook03 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c3e75-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c3e75-110">OS</span><span class="sxs-lookup"><span data-stu-id="c3e75-110">PARAMETERS</span></span>

### <span data-ttu-id="c3e75-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c3e75-111">-AutomationAccountName</span></span>
<span data-ttu-id="c3e75-112">Especifica o nome da conta de automação na qual esse cmdlet Remove um runbook.</span><span class="sxs-lookup"><span data-stu-id="c3e75-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="c3e75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e75-113">-DefaultProfile</span></span>
<span data-ttu-id="c3e75-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c3e75-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e75-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c3e75-115">-Force</span></span>
<span data-ttu-id="c3e75-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="c3e75-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e75-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3e75-117">-Name</span></span>
<span data-ttu-id="c3e75-118">Especifica o nome do runbook que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c3e75-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e75-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e75-119">-ResourceGroupName</span></span>
<span data-ttu-id="c3e75-120">Especifica o nome do grupo de recursos para o qual esse cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="c3e75-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="c3e75-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3e75-121">-Confirm</span></span>
<span data-ttu-id="c3e75-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e75-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e75-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e75-123">-WhatIf</span></span>
<span data-ttu-id="c3e75-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3e75-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e75-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3e75-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e75-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e75-126">CommonParameters</span></span>
<span data-ttu-id="c3e75-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e75-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e75-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e75-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e75-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3e75-129">INPUTS</span></span>

### <span data-ttu-id="c3e75-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c3e75-130">None</span></span>
<span data-ttu-id="c3e75-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c3e75-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3e75-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3e75-132">OUTPUTS</span></span>

## <span data-ttu-id="c3e75-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3e75-133">NOTES</span></span>

## <span data-ttu-id="c3e75-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3e75-134">RELATED LINKS</span></span>

[<span data-ttu-id="c3e75-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c3e75-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c3e75-137">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c3e75-138">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c3e75-139">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c3e75-140">Publicar-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c3e75-141">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-141">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c3e75-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c3e75-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)

