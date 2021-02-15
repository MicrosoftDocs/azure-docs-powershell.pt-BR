---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117994"
---
# <span data-ttu-id="2db2c-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="2db2c-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="2db2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2db2c-102">SYNOPSIS</span></span>
<span data-ttu-id="2db2c-103">Remove um controle de origem da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="2db2c-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="2db2c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2db2c-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2db2c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2db2c-105">DESCRIPTION</span></span>
<span data-ttu-id="2db2c-106">O Remove-AzAutomationSourceControl cmdlet remove um controle de origem da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="2db2c-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="2db2c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2db2c-107">EXAMPLES</span></span>

### <span data-ttu-id="2db2c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2db2c-108">Example 1</span></span>
<span data-ttu-id="2db2c-109">Esse comando remove o controle de origem automação chamado VSTSNative na conta chamada devAccount.</span><span class="sxs-lookup"><span data-stu-id="2db2c-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="2db2c-110">Esse comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="2db2c-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="2db2c-111">Portanto, ele não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="2db2c-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="2db2c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2db2c-112">PARAMETERS</span></span>

### <span data-ttu-id="2db2c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2db2c-113">-AutomationAccountName</span></span>
<span data-ttu-id="2db2c-114">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="2db2c-114">The automation account name.</span></span>

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

### <span data-ttu-id="2db2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db2c-115">-DefaultProfile</span></span>
<span data-ttu-id="2db2c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2db2c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db2c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2db2c-117">-Name</span></span>
<span data-ttu-id="2db2c-118">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="2db2c-118">The source control name.</span></span>

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

### <span data-ttu-id="2db2c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2db2c-119">-PassThru</span></span>
<span data-ttu-id="2db2c-120">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2db2c-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2db2c-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="2db2c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2db2c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db2c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2db2c-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2db2c-123">The resource group name.</span></span>

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

### <span data-ttu-id="2db2c-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2db2c-124">-Confirm</span></span>
<span data-ttu-id="2db2c-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2db2c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db2c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db2c-126">-WhatIf</span></span>
<span data-ttu-id="2db2c-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2db2c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2db2c-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2db2c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db2c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db2c-129">CommonParameters</span></span>
<span data-ttu-id="2db2c-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db2c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db2c-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db2c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db2c-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="2db2c-132">INPUTS</span></span>

### <span data-ttu-id="2db2c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2db2c-133">System.String</span></span>

## <span data-ttu-id="2db2c-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="2db2c-134">OUTPUTS</span></span>

### <span data-ttu-id="2db2c-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="2db2c-135">System.Void</span></span>

### <span data-ttu-id="2db2c-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2db2c-136">System.Boolean</span></span>

## <span data-ttu-id="2db2c-137">Notas</span><span class="sxs-lookup"><span data-stu-id="2db2c-137">NOTES</span></span>

## <span data-ttu-id="2db2c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2db2c-138">RELATED LINKS</span></span>
