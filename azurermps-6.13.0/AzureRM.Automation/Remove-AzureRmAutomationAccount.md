---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: e3dd0d475a2a2c34dfa7912bf9ced4ef958295c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428627"
---
# <span data-ttu-id="721f6-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="721f6-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="721f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="721f6-102">SYNOPSIS</span></span>
<span data-ttu-id="721f6-103">Remove uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="721f6-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="721f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="721f6-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="721f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="721f6-105">DESCRIPTION</span></span>
<span data-ttu-id="721f6-106">O cmdlet **Remove-AzureRmAutomationAccount** remove uma conta de automação do Azure de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="721f6-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="721f6-107">Para obter mais informações sobre contas de automação, consulte o cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="721f6-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="721f6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="721f6-108">EXAMPLES</span></span>

### <span data-ttu-id="721f6-109">Exemplo 1: remover uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="721f6-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="721f6-110">Esse comando Remove uma conta de automação chamada ContosoAutomationAccount sem solicitar a validação do usuário.</span><span class="sxs-lookup"><span data-stu-id="721f6-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="721f6-111">OS</span><span class="sxs-lookup"><span data-stu-id="721f6-111">PARAMETERS</span></span>

### <span data-ttu-id="721f6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721f6-112">-DefaultProfile</span></span>
<span data-ttu-id="721f6-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="721f6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="721f6-114">-Force</span><span class="sxs-lookup"><span data-stu-id="721f6-114">-Force</span></span>
<span data-ttu-id="721f6-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="721f6-115">ps_force</span></span>

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

### <span data-ttu-id="721f6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="721f6-116">-Name</span></span>
<span data-ttu-id="721f6-117">Especifica o nome da conta de automação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="721f6-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="721f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="721f6-119">Especifica o nome do grupo de recursos do qual esse cmdlet Remove uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="721f6-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="721f6-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="721f6-120">-Confirm</span></span>
<span data-ttu-id="721f6-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="721f6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="721f6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="721f6-122">-WhatIf</span></span>
<span data-ttu-id="721f6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="721f6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="721f6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="721f6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="721f6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721f6-125">CommonParameters</span></span>
<span data-ttu-id="721f6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721f6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721f6-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="721f6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721f6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="721f6-128">INPUTS</span></span>

### <span data-ttu-id="721f6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="721f6-129">System.String</span></span>

## <span data-ttu-id="721f6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="721f6-130">OUTPUTS</span></span>

### <span data-ttu-id="721f6-131">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="721f6-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="721f6-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="721f6-132">NOTES</span></span>

## <span data-ttu-id="721f6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="721f6-133">RELATED LINKS</span></span>

[<span data-ttu-id="721f6-134">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="721f6-134">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="721f6-135">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="721f6-135">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="721f6-136">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="721f6-136">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


