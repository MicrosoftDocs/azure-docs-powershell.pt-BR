---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6c0e557078bde5cbec7b1f7dd96f1fa2c71408a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775266"
---
# <span data-ttu-id="e454f-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="e454f-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="e454f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e454f-102">SYNOPSIS</span></span>
<span data-ttu-id="e454f-103">Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e454f-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="e454f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e454f-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e454f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e454f-105">DESCRIPTION</span></span>
<span data-ttu-id="e454f-106">Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e454f-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="e454f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e454f-107">EXAMPLES</span></span>

### <span data-ttu-id="e454f-108">Habilitar a gravação simultânea de credenciais para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="e454f-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="e454f-109">Ative o salvamento automático de credenciais para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="e454f-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="e454f-110">Sempre que uma janela do PowerShell é aberta, seu contexto atual será lembrado sem fazer logon.</span><span class="sxs-lookup"><span data-stu-id="e454f-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="e454f-111">OS</span><span class="sxs-lookup"><span data-stu-id="e454f-111">PARAMETERS</span></span>

### <span data-ttu-id="e454f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e454f-112">-DefaultProfile</span></span>
<span data-ttu-id="e454f-113">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e454f-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e454f-114">-Escopo</span><span class="sxs-lookup"><span data-stu-id="e454f-114">-Scope</span></span>
<span data-ttu-id="e454f-115">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="e454f-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="e454f-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e454f-116">-Confirm</span></span>
<span data-ttu-id="e454f-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e454f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e454f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e454f-118">-WhatIf</span></span>
<span data-ttu-id="e454f-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e454f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e454f-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e454f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e454f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e454f-121">CommonParameters</span></span>
<span data-ttu-id="e454f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e454f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e454f-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e454f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e454f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e454f-124">INPUTS</span></span>

### <span data-ttu-id="e454f-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e454f-125">None</span></span>

## <span data-ttu-id="e454f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e454f-126">OUTPUTS</span></span>

### <span data-ttu-id="e454f-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="e454f-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="e454f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e454f-128">NOTES</span></span>

## <span data-ttu-id="e454f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e454f-129">RELATED LINKS</span></span>