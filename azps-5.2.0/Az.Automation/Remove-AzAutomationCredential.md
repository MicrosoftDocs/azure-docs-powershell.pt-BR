---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264528"
---
# <span data-ttu-id="e9a41-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e9a41-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="e9a41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9a41-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a41-103">Remove uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="e9a41-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="e9a41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9a41-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9a41-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9a41-105">DESCRIPTION</span></span>
<span data-ttu-id="e9a41-106">O cmdlet **Remove-AzAutomationCredential** remove uma credencial da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a41-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="e9a41-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9a41-107">EXAMPLES</span></span>

### <span data-ttu-id="e9a41-108">Exemplo 1: remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="e9a41-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e9a41-109">Esse comando Remove uma credencial chamada ContosoCredential na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e9a41-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e9a41-110">OS</span><span class="sxs-lookup"><span data-stu-id="e9a41-110">PARAMETERS</span></span>

### <span data-ttu-id="e9a41-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9a41-111">-AutomationAccountName</span></span>
<span data-ttu-id="e9a41-112">Especifica o nome da conta de automação a partir da qual esse cmdlet Remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="e9a41-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="e9a41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a41-113">-DefaultProfile</span></span>
<span data-ttu-id="e9a41-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e9a41-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9a41-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9a41-115">-Name</span></span>
<span data-ttu-id="e9a41-116">Especifica o nome da credencial que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e9a41-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9a41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a41-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9a41-118">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="e9a41-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="e9a41-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9a41-119">-Confirm</span></span>
<span data-ttu-id="e9a41-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9a41-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a41-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a41-121">-WhatIf</span></span>
<span data-ttu-id="e9a41-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9a41-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9a41-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9a41-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9a41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a41-124">CommonParameters</span></span>
<span data-ttu-id="e9a41-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a41-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9a41-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a41-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9a41-127">INPUTS</span></span>

### <span data-ttu-id="e9a41-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e9a41-128">System.String</span></span>

## <span data-ttu-id="e9a41-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9a41-129">OUTPUTS</span></span>

### <span data-ttu-id="e9a41-130">System. void</span><span class="sxs-lookup"><span data-stu-id="e9a41-130">System.Void</span></span>

## <span data-ttu-id="e9a41-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9a41-131">NOTES</span></span>

## <span data-ttu-id="e9a41-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9a41-132">RELATED LINKS</span></span>

[<span data-ttu-id="e9a41-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e9a41-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="e9a41-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e9a41-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="e9a41-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e9a41-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


