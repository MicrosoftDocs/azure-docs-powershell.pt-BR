---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 854a5bd2fb9644d6060810edba44ac7082eb6903
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430525"
---
# <span data-ttu-id="63304-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="63304-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="63304-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63304-102">SYNOPSIS</span></span>
<span data-ttu-id="63304-103">Remove uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="63304-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63304-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63304-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63304-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63304-105">DESCRIPTION</span></span>
<span data-ttu-id="63304-106">O cmdlet **Remove-AzureRmAutomationAccount** remove uma conta de automação do Azure de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="63304-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="63304-107">Para obter mais informações sobre contas de automação, consulte o cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="63304-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="63304-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63304-108">EXAMPLES</span></span>

### <span data-ttu-id="63304-109">Exemplo 1: remover uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="63304-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="63304-110">Esse comando Remove uma conta de automação chamada ContosoAutomationAccount sem solicitar a validação do usuário.</span><span class="sxs-lookup"><span data-stu-id="63304-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="63304-111">OS</span><span class="sxs-lookup"><span data-stu-id="63304-111">PARAMETERS</span></span>

### <span data-ttu-id="63304-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63304-112">-DefaultProfile</span></span>
<span data-ttu-id="63304-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="63304-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63304-114">-Force</span><span class="sxs-lookup"><span data-stu-id="63304-114">-Force</span></span>
<span data-ttu-id="63304-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="63304-115">ps_force</span></span>

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

### <span data-ttu-id="63304-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="63304-116">-Name</span></span>
<span data-ttu-id="63304-117">Especifica o nome da conta de automação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="63304-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63304-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63304-118">-ResourceGroupName</span></span>
<span data-ttu-id="63304-119">Especifica o nome do grupo de recursos do qual esse cmdlet Remove uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="63304-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="63304-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="63304-120">-Confirm</span></span>
<span data-ttu-id="63304-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63304-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63304-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63304-122">-WhatIf</span></span>
<span data-ttu-id="63304-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63304-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63304-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63304-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63304-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63304-125">CommonParameters</span></span>
<span data-ttu-id="63304-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63304-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63304-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63304-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63304-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63304-128">INPUTS</span></span>

### <span data-ttu-id="63304-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="63304-129">None</span></span>
<span data-ttu-id="63304-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="63304-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63304-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63304-131">OUTPUTS</span></span>

### <span data-ttu-id="63304-132">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="63304-132">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="63304-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63304-133">NOTES</span></span>

## <span data-ttu-id="63304-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63304-134">RELATED LINKS</span></span>

[<span data-ttu-id="63304-135">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="63304-135">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="63304-136">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="63304-136">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="63304-137">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="63304-137">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


