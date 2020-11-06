---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 703be26244e61b797f3359ef508d92e38847bf8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597768"
---
# <span data-ttu-id="ffd64-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ffd64-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="ffd64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffd64-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd64-103">Remove uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="ffd64-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="ffd64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffd64-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffd64-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffd64-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd64-106">O cmdlet **Remove-AzAutomationCredential** remove uma credencial da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd64-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="ffd64-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffd64-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd64-108">Exemplo 1: remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="ffd64-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ffd64-109">Esse comando Remove uma credencial chamada ContosoCredential na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ffd64-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ffd64-110">OS</span><span class="sxs-lookup"><span data-stu-id="ffd64-110">PARAMETERS</span></span>

### <span data-ttu-id="ffd64-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ffd64-111">-AutomationAccountName</span></span>
<span data-ttu-id="ffd64-112">Especifica o nome da conta de automação a partir da qual esse cmdlet Remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="ffd64-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="ffd64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd64-113">-DefaultProfile</span></span>
<span data-ttu-id="ffd64-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ffd64-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffd64-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffd64-115">-Name</span></span>
<span data-ttu-id="ffd64-116">Especifica o nome da credencial que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ffd64-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ffd64-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd64-117">-ResourceGroupName</span></span>
<span data-ttu-id="ffd64-118">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="ffd64-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="ffd64-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffd64-119">-Confirm</span></span>
<span data-ttu-id="ffd64-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffd64-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd64-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd64-121">-WhatIf</span></span>
<span data-ttu-id="ffd64-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffd64-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd64-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffd64-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd64-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd64-124">CommonParameters</span></span>
<span data-ttu-id="ffd64-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd64-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd64-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd64-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd64-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffd64-127">INPUTS</span></span>

### <span data-ttu-id="ffd64-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ffd64-128">System.String</span></span>

## <span data-ttu-id="ffd64-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffd64-129">OUTPUTS</span></span>

### <span data-ttu-id="ffd64-130">System. void</span><span class="sxs-lookup"><span data-stu-id="ffd64-130">System.Void</span></span>

## <span data-ttu-id="ffd64-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffd64-131">NOTES</span></span>

## <span data-ttu-id="ffd64-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffd64-132">RELATED LINKS</span></span>

[<span data-ttu-id="ffd64-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ffd64-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="ffd64-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ffd64-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="ffd64-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ffd64-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


