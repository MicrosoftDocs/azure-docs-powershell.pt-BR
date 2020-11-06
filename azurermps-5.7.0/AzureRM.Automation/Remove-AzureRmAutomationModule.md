---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 2ce97441769c15ed122dc7921554b4fa1c5a144f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441492"
---
# <span data-ttu-id="cb711-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cb711-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="cb711-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb711-102">SYNOPSIS</span></span>
<span data-ttu-id="cb711-103">Remove um módulo da automação.</span><span class="sxs-lookup"><span data-stu-id="cb711-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb711-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb711-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb711-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb711-105">DESCRIPTION</span></span>
<span data-ttu-id="cb711-106">O cmdlet **Remove-AzureRmAutomationModule** remove um módulo de uma conta de automação na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb711-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="cb711-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb711-107">EXAMPLES</span></span>

### <span data-ttu-id="cb711-108">Exemplo 1: remover um módulo</span><span class="sxs-lookup"><span data-stu-id="cb711-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cb711-109">Esse comando Remove um módulo chamado ContosoModule da conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cb711-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cb711-110">OS</span><span class="sxs-lookup"><span data-stu-id="cb711-110">PARAMETERS</span></span>

### <span data-ttu-id="cb711-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cb711-111">-AutomationAccountName</span></span>
<span data-ttu-id="cb711-112">Especifica o nome da conta de automação a partir da qual esse cmdlet Remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="cb711-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="cb711-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb711-113">-DefaultProfile</span></span>
<span data-ttu-id="cb711-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cb711-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb711-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cb711-115">-Force</span></span>
<span data-ttu-id="cb711-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="cb711-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb711-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb711-117">-Name</span></span>
<span data-ttu-id="cb711-118">Especifica o nome do módulo que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="cb711-118">Specifies the name of the module that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb711-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb711-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb711-120">Especifica o nome de um grupo de recursos em que esse cmdlet Remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="cb711-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="cb711-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb711-121">-Confirm</span></span>
<span data-ttu-id="cb711-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb711-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb711-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb711-123">-WhatIf</span></span>
<span data-ttu-id="cb711-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb711-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb711-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb711-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb711-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb711-126">CommonParameters</span></span>
<span data-ttu-id="cb711-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb711-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb711-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb711-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb711-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb711-129">INPUTS</span></span>

### <span data-ttu-id="cb711-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cb711-130">None</span></span>
<span data-ttu-id="cb711-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="cb711-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb711-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb711-132">OUTPUTS</span></span>

## <span data-ttu-id="cb711-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb711-133">NOTES</span></span>

## <span data-ttu-id="cb711-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb711-134">RELATED LINKS</span></span>

[<span data-ttu-id="cb711-135">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cb711-135">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="cb711-136">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cb711-136">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="cb711-137">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cb711-137">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


