---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 8db930fe362d25a7b1069af6c3855ef71644e874
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890326"
---
# <span data-ttu-id="9497e-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="9497e-101">Clear-AzContext</span></span>

## <span data-ttu-id="9497e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9497e-102">SYNOPSIS</span></span>
<span data-ttu-id="9497e-103">Remova todas as credenciais, contas e informações de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="9497e-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="9497e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9497e-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9497e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9497e-105">DESCRIPTION</span></span>
<span data-ttu-id="9497e-106">Remova todas as credenciais, conta e informações de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="9497e-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="9497e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9497e-107">EXAMPLES</span></span>

### <span data-ttu-id="9497e-108">Exemplo 1: Limpar contexto global</span><span class="sxs-lookup"><span data-stu-id="9497e-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="9497e-109">Remova todas as informações de conta, assinatura e credencial para qualquer sessão do powershell.</span><span class="sxs-lookup"><span data-stu-id="9497e-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="9497e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9497e-110">PARAMETERS</span></span>

### <span data-ttu-id="9497e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9497e-111">-DefaultProfile</span></span>
<span data-ttu-id="9497e-112">As credenciais, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9497e-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9497e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9497e-113">-Force</span></span>
<span data-ttu-id="9497e-114">Excluir todos os usuários e grupos do escopo global sem solicitar</span><span class="sxs-lookup"><span data-stu-id="9497e-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="9497e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9497e-115">-PassThru</span></span>
<span data-ttu-id="9497e-116">Retornar um valor que indica sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="9497e-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="9497e-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="9497e-117">-Scope</span></span>
<span data-ttu-id="9497e-118">Limpe o contexto apenas para a sessão atual do PowerShell ou para todas as sessões.</span><span class="sxs-lookup"><span data-stu-id="9497e-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9497e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9497e-119">-Confirm</span></span>
<span data-ttu-id="9497e-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9497e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9497e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9497e-121">-WhatIf</span></span>
<span data-ttu-id="9497e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9497e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9497e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9497e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9497e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9497e-124">CommonParameters</span></span>
<span data-ttu-id="9497e-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9497e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9497e-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9497e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9497e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9497e-127">INPUTS</span></span>

### <span data-ttu-id="9497e-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9497e-128">None</span></span>

## <span data-ttu-id="9497e-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9497e-129">OUTPUTS</span></span>

### <span data-ttu-id="9497e-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9497e-130">System.Boolean</span></span>

## <span data-ttu-id="9497e-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="9497e-131">NOTES</span></span>

## <span data-ttu-id="9497e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9497e-132">RELATED LINKS</span></span>
