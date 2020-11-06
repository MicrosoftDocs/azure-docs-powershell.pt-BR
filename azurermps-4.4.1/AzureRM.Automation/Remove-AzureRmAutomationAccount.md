---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 1b8e480a266459b21e6c357da156b4d4bc5165e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431174"
---
# <span data-ttu-id="4bc5f-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4bc5f-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="4bc5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc5f-103">Remove uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bc5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bc5f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bc5f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4bc5f-105">DESCRIPTION</span></span>
<span data-ttu-id="4bc5f-106">O cmdlet **Remove-AzureRmAutomationAccount** remove uma conta de automação do Azure de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="4bc5f-107">Para obter mais informações sobre contas de automação, consulte o cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="4bc5f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4bc5f-108">EXAMPLES</span></span>

### <span data-ttu-id="4bc5f-109">Exemplo 1: remover uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="4bc5f-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4bc5f-110">Esse comando Remove uma conta de automação chamada ContosoAutomationAccount sem solicitar a validação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="4bc5f-111">OS</span><span class="sxs-lookup"><span data-stu-id="4bc5f-111">PARAMETERS</span></span>

### <span data-ttu-id="4bc5f-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4bc5f-112">-Force</span></span>
<span data-ttu-id="4bc5f-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="4bc5f-113">ps_force</span></span>

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

### <span data-ttu-id="4bc5f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bc5f-114">-Name</span></span>
<span data-ttu-id="4bc5f-115">Especifica o nome da conta de automação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-115">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4bc5f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc5f-116">-ResourceGroupName</span></span>
<span data-ttu-id="4bc5f-117">Especifica o nome do grupo de recursos do qual esse cmdlet Remove uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-117">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="4bc5f-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4bc5f-118">-Confirm</span></span>
<span data-ttu-id="4bc5f-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bc5f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc5f-120">-WhatIf</span></span>
<span data-ttu-id="4bc5f-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bc5f-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bc5f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc5f-123">-DefaultProfile</span></span>
<span data-ttu-id="4bc5f-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bc5f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc5f-125">CommonParameters</span></span>
<span data-ttu-id="4bc5f-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc5f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc5f-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bc5f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc5f-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4bc5f-128">INPUTS</span></span>

## <span data-ttu-id="4bc5f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4bc5f-129">OUTPUTS</span></span>

### <span data-ttu-id="4bc5f-130">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4bc5f-130">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="4bc5f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4bc5f-131">NOTES</span></span>

## <span data-ttu-id="4bc5f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bc5f-132">RELATED LINKS</span></span>

[<span data-ttu-id="4bc5f-133">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4bc5f-133">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="4bc5f-134">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4bc5f-134">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="4bc5f-135">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4bc5f-135">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


