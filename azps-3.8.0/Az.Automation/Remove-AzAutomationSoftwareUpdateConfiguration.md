---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944920"
---
# <span data-ttu-id="6e007-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e007-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6e007-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e007-102">SYNOPSIS</span></span>
<span data-ttu-id="6e007-103">Remove uma configuração de atualização do software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e007-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="6e007-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e007-104">SYNTAX</span></span>

### <span data-ttu-id="6e007-105">BySucName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6e007-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e007-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="6e007-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e007-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e007-107">DESCRIPTION</span></span>
<span data-ttu-id="6e007-108">Este cmdlet removeu uma configuração de atualização do software de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e007-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="6e007-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e007-109">EXAMPLES</span></span>

### <span data-ttu-id="6e007-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e007-110">Example 1</span></span>
<span data-ttu-id="6e007-111">Este exemplo mostra como remover "MyUpdateConfiguration" da conta de automação</span><span class="sxs-lookup"><span data-stu-id="6e007-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="6e007-112">OS</span><span class="sxs-lookup"><span data-stu-id="6e007-112">PARAMETERS</span></span>

### <span data-ttu-id="6e007-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6e007-113">-AutomationAccountName</span></span>
<span data-ttu-id="6e007-114">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="6e007-114">The automation account name.</span></span>

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

### <span data-ttu-id="6e007-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e007-115">-DefaultProfile</span></span>
<span data-ttu-id="6e007-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e007-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e007-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e007-117">-Name</span></span>
<span data-ttu-id="6e007-118">Nome da configuração de atualização de software a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6e007-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="6e007-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e007-119">-PassThru</span></span>
<span data-ttu-id="6e007-120">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="6e007-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6e007-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6e007-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e007-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e007-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e007-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e007-123">The resource group name.</span></span>

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

### <span data-ttu-id="6e007-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e007-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="6e007-125">A configuração de atualização de software a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6e007-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="6e007-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e007-126">-Confirm</span></span>
<span data-ttu-id="6e007-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e007-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e007-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e007-128">-WhatIf</span></span>
<span data-ttu-id="6e007-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e007-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e007-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e007-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e007-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e007-131">CommonParameters</span></span>
<span data-ttu-id="6e007-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e007-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e007-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e007-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e007-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e007-134">INPUTS</span></span>

### <span data-ttu-id="6e007-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6e007-135">System.String</span></span>

### <span data-ttu-id="6e007-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e007-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6e007-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e007-137">OUTPUTS</span></span>

### <span data-ttu-id="6e007-138">System. void</span><span class="sxs-lookup"><span data-stu-id="6e007-138">System.Void</span></span>

### <span data-ttu-id="6e007-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e007-139">System.Boolean</span></span>

## <span data-ttu-id="6e007-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e007-140">NOTES</span></span>

## <span data-ttu-id="6e007-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e007-141">RELATED LINKS</span></span>
