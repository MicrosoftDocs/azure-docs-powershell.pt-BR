---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 8ddc84e3fac5df9253ffdacb61d4f4c7a5568c6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886106"
---
# <span data-ttu-id="b1230-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1230-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="b1230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1230-102">SYNOPSIS</span></span>
<span data-ttu-id="b1230-103">Remove uma configuração de atualização de software de automação do azure.</span><span class="sxs-lookup"><span data-stu-id="b1230-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="b1230-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b1230-104">SYNTAX</span></span>

### <span data-ttu-id="b1230-105">BySucName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b1230-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1230-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="b1230-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1230-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b1230-107">DESCRIPTION</span></span>
<span data-ttu-id="b1230-108">Este cmdlet removeu uma configuração de atualização de software de automação do azure.</span><span class="sxs-lookup"><span data-stu-id="b1230-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="b1230-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1230-109">EXAMPLES</span></span>

### <span data-ttu-id="b1230-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1230-110">Example 1</span></span>
<span data-ttu-id="b1230-111">Este exemplo mostra como remover 'MyUpdateConfiguration' da conta de automação</span><span class="sxs-lookup"><span data-stu-id="b1230-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="b1230-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b1230-112">PARAMETERS</span></span>

### <span data-ttu-id="b1230-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b1230-113">-AutomationAccountName</span></span>
<span data-ttu-id="b1230-114">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="b1230-114">The automation account name.</span></span>

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

### <span data-ttu-id="b1230-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1230-115">-DefaultProfile</span></span>
<span data-ttu-id="b1230-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1230-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1230-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b1230-117">-Name</span></span>
<span data-ttu-id="b1230-118">Nome da configuração de atualização de software a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b1230-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1230-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1230-119">-PassThru</span></span>
<span data-ttu-id="b1230-120">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b1230-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b1230-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b1230-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1230-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1230-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1230-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1230-123">The resource group name.</span></span>

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

### <span data-ttu-id="b1230-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1230-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="b1230-125">A configuração de atualização de software a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b1230-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1230-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1230-126">-Confirm</span></span>
<span data-ttu-id="b1230-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1230-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1230-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1230-128">-WhatIf</span></span>
<span data-ttu-id="b1230-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1230-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1230-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1230-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1230-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1230-131">CommonParameters</span></span>
<span data-ttu-id="b1230-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1230-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1230-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1230-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1230-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1230-134">INPUTS</span></span>

### <span data-ttu-id="b1230-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b1230-135">System.String</span></span>

### <span data-ttu-id="b1230-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1230-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="b1230-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b1230-137">OUTPUTS</span></span>

### <span data-ttu-id="b1230-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="b1230-138">System.Void</span></span>

### <span data-ttu-id="b1230-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1230-139">System.Boolean</span></span>

## <span data-ttu-id="b1230-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="b1230-140">NOTES</span></span>

## <span data-ttu-id="b1230-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1230-141">RELATED LINKS</span></span>
