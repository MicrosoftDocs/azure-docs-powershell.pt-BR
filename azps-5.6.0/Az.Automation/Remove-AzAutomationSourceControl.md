---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: b4e60e4bbc7196736c0e49c2b294cf6cb984e7b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892884"
---
# <span data-ttu-id="44f72-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="44f72-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="44f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44f72-102">SYNOPSIS</span></span>
<span data-ttu-id="44f72-103">Remove um controle de origem da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="44f72-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="44f72-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="44f72-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44f72-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="44f72-105">DESCRIPTION</span></span>
<span data-ttu-id="44f72-106">O Remove-AzAutomationSourceControl cmdlet remove um controle de origem da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="44f72-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="44f72-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44f72-107">EXAMPLES</span></span>

### <span data-ttu-id="44f72-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44f72-108">Example 1</span></span>
<span data-ttu-id="44f72-109">Este comando remove o controle de origem de automação chamado VSTSNative na conta chamada devAccount.</span><span class="sxs-lookup"><span data-stu-id="44f72-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="44f72-110">Este comando especifica o *parâmetro Force.*</span><span class="sxs-lookup"><span data-stu-id="44f72-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="44f72-111">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="44f72-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="44f72-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="44f72-112">PARAMETERS</span></span>

### <span data-ttu-id="44f72-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="44f72-113">-AutomationAccountName</span></span>
<span data-ttu-id="44f72-114">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="44f72-114">The automation account name.</span></span>

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

### <span data-ttu-id="44f72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f72-115">-DefaultProfile</span></span>
<span data-ttu-id="44f72-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44f72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44f72-117">-Name</span><span class="sxs-lookup"><span data-stu-id="44f72-117">-Name</span></span>
<span data-ttu-id="44f72-118">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="44f72-118">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f72-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44f72-119">-PassThru</span></span>
<span data-ttu-id="44f72-120">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="44f72-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="44f72-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="44f72-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44f72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f72-122">-ResourceGroupName</span></span>
<span data-ttu-id="44f72-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44f72-123">The resource group name.</span></span>

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

### <span data-ttu-id="44f72-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44f72-124">-Confirm</span></span>
<span data-ttu-id="44f72-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44f72-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44f72-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44f72-126">-WhatIf</span></span>
<span data-ttu-id="44f72-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44f72-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44f72-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44f72-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44f72-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f72-129">CommonParameters</span></span>
<span data-ttu-id="44f72-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f72-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f72-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44f72-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f72-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44f72-132">INPUTS</span></span>

### <span data-ttu-id="44f72-133">System.String</span><span class="sxs-lookup"><span data-stu-id="44f72-133">System.String</span></span>

## <span data-ttu-id="44f72-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="44f72-134">OUTPUTS</span></span>

### <span data-ttu-id="44f72-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="44f72-135">System.Void</span></span>

### <span data-ttu-id="44f72-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44f72-136">System.Boolean</span></span>

## <span data-ttu-id="44f72-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="44f72-137">NOTES</span></span>

## <span data-ttu-id="44f72-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44f72-138">RELATED LINKS</span></span>
