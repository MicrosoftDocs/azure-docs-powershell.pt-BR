---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116701"
---
# <span data-ttu-id="4f30f-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="4f30f-101">Clear-AzContext</span></span>

## <span data-ttu-id="4f30f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f30f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f30f-103">Remova todas as credenciais, contas e informações de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f30f-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="4f30f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f30f-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f30f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f30f-105">DESCRIPTION</span></span>
<span data-ttu-id="4f30f-106">Remova todas as credenciais, contas e informações de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f30f-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="4f30f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f30f-107">EXAMPLES</span></span>

### <span data-ttu-id="4f30f-108">Exemplo 1: Limpar contexto global</span><span class="sxs-lookup"><span data-stu-id="4f30f-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="4f30f-109">Remova todas as informações de conta, assinatura e credencial de qualquer sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4f30f-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="4f30f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f30f-110">PARAMETERS</span></span>

### <span data-ttu-id="4f30f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f30f-111">-DefaultProfile</span></span>
<span data-ttu-id="4f30f-112">As credenciais, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4f30f-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f30f-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4f30f-113">-Force</span></span>
<span data-ttu-id="4f30f-114">Excluir todos os usuários e grupos do escopo global sem solicitar</span><span class="sxs-lookup"><span data-stu-id="4f30f-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="4f30f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f30f-115">-PassThru</span></span>
<span data-ttu-id="4f30f-116">Retornar um valor indicando sucesso ou fracasso</span><span class="sxs-lookup"><span data-stu-id="4f30f-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="4f30f-117">-Escopo</span><span class="sxs-lookup"><span data-stu-id="4f30f-117">-Scope</span></span>
<span data-ttu-id="4f30f-118">Limpe o contexto somente para a sessão atual do PowerShell ou para todas as sessões.</span><span class="sxs-lookup"><span data-stu-id="4f30f-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="4f30f-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4f30f-119">-Confirm</span></span>
<span data-ttu-id="4f30f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f30f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f30f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f30f-121">-WhatIf</span></span>
<span data-ttu-id="4f30f-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4f30f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f30f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f30f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f30f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f30f-124">CommonParameters</span></span>
<span data-ttu-id="4f30f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f30f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f30f-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f30f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f30f-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="4f30f-127">INPUTS</span></span>

### <span data-ttu-id="4f30f-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4f30f-128">None</span></span>

## <span data-ttu-id="4f30f-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="4f30f-129">OUTPUTS</span></span>

### <span data-ttu-id="4f30f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f30f-130">System.Boolean</span></span>

## <span data-ttu-id="4f30f-131">Notas</span><span class="sxs-lookup"><span data-stu-id="4f30f-131">NOTES</span></span>

## <span data-ttu-id="4f30f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f30f-132">RELATED LINKS</span></span>
