---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115118"
---
# <span data-ttu-id="1d413-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="1d413-101">Clear-AzContext</span></span>

## <span data-ttu-id="1d413-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d413-102">SYNOPSIS</span></span>
<span data-ttu-id="1d413-103">Remova todas as credenciais do Azure, conta e informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="1d413-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="1d413-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d413-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d413-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d413-105">DESCRIPTION</span></span>
<span data-ttu-id="1d413-106">Remova todas as credenciais do Azure, conta e informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="1d413-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="1d413-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d413-107">EXAMPLES</span></span>

### <span data-ttu-id="1d413-108">Exemplo 1: limpar contexto global</span><span class="sxs-lookup"><span data-stu-id="1d413-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="1d413-109">Remova todas as informações de conta, assinatura e credenciais para qualquer sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1d413-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="1d413-110">OS</span><span class="sxs-lookup"><span data-stu-id="1d413-110">PARAMETERS</span></span>

### <span data-ttu-id="1d413-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d413-111">-DefaultProfile</span></span>
<span data-ttu-id="1d413-112">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1d413-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d413-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1d413-113">-Force</span></span>
<span data-ttu-id="1d413-114">Excluir todos os usuários e grupos do escopo global sem solicitação</span><span class="sxs-lookup"><span data-stu-id="1d413-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="1d413-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d413-115">-PassThru</span></span>
<span data-ttu-id="1d413-116">Retornar um valor que indica êxito ou falha</span><span class="sxs-lookup"><span data-stu-id="1d413-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="1d413-117">-Escopo</span><span class="sxs-lookup"><span data-stu-id="1d413-117">-Scope</span></span>
<span data-ttu-id="1d413-118">Limpe o contexto somente para a sessão atual do PowerShell ou para todas as sessões.</span><span class="sxs-lookup"><span data-stu-id="1d413-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="1d413-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1d413-119">-Confirm</span></span>
<span data-ttu-id="1d413-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d413-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d413-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d413-121">-WhatIf</span></span>
<span data-ttu-id="1d413-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d413-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d413-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d413-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d413-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d413-124">CommonParameters</span></span>
<span data-ttu-id="1d413-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d413-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d413-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d413-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d413-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d413-127">INPUTS</span></span>

### <span data-ttu-id="1d413-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1d413-128">None</span></span>

## <span data-ttu-id="1d413-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d413-129">OUTPUTS</span></span>

### <span data-ttu-id="1d413-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d413-130">System.Boolean</span></span>

## <span data-ttu-id="1d413-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d413-131">NOTES</span></span>

## <span data-ttu-id="1d413-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d413-132">RELATED LINKS</span></span>
