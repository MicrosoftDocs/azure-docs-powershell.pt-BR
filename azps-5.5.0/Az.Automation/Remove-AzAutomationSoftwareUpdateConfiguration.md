---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117996"
---
# <span data-ttu-id="0aaf2-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aaf2-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="0aaf2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0aaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="0aaf2-103">Remove uma configuração de atualização de software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="0aaf2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0aaf2-104">SYNTAX</span></span>

### <span data-ttu-id="0aaf2-105">BySucName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0aaf2-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0aaf2-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="0aaf2-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aaf2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0aaf2-107">DESCRIPTION</span></span>
<span data-ttu-id="0aaf2-108">Este cmdlet removeu uma configuração de atualização de software de automação do azure.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="0aaf2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0aaf2-109">EXAMPLES</span></span>

### <span data-ttu-id="0aaf2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0aaf2-110">Example 1</span></span>
<span data-ttu-id="0aaf2-111">Este exemplo mostra como remover "MyUpdateConfiguration" da conta de automação</span><span class="sxs-lookup"><span data-stu-id="0aaf2-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="0aaf2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0aaf2-112">PARAMETERS</span></span>

### <span data-ttu-id="0aaf2-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0aaf2-113">-AutomationAccountName</span></span>
<span data-ttu-id="0aaf2-114">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-114">The automation account name.</span></span>

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

### <span data-ttu-id="0aaf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aaf2-115">-DefaultProfile</span></span>
<span data-ttu-id="0aaf2-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aaf2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0aaf2-117">-Name</span></span>
<span data-ttu-id="0aaf2-118">Nome da configuração de atualização de software a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="0aaf2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0aaf2-119">-PassThru</span></span>
<span data-ttu-id="0aaf2-120">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="0aaf2-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0aaf2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aaf2-122">-ResourceGroupName</span></span>
<span data-ttu-id="0aaf2-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-123">The resource group name.</span></span>

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

### <span data-ttu-id="0aaf2-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aaf2-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="0aaf2-125">A configuração de atualização de software a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="0aaf2-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0aaf2-126">-Confirm</span></span>
<span data-ttu-id="0aaf2-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aaf2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aaf2-128">-WhatIf</span></span>
<span data-ttu-id="0aaf2-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aaf2-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aaf2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aaf2-131">CommonParameters</span></span>
<span data-ttu-id="0aaf2-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aaf2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aaf2-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aaf2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aaf2-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="0aaf2-134">INPUTS</span></span>

### <span data-ttu-id="0aaf2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0aaf2-135">System.String</span></span>

### <span data-ttu-id="0aaf2-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aaf2-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="0aaf2-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="0aaf2-137">OUTPUTS</span></span>

### <span data-ttu-id="0aaf2-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="0aaf2-138">System.Void</span></span>

### <span data-ttu-id="0aaf2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0aaf2-139">System.Boolean</span></span>

## <span data-ttu-id="0aaf2-140">Notas</span><span class="sxs-lookup"><span data-stu-id="0aaf2-140">NOTES</span></span>

## <span data-ttu-id="0aaf2-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0aaf2-141">RELATED LINKS</span></span>
