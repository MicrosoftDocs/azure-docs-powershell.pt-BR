---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: c5d01fcc7ba007a0336fac5c08db44b840e75806
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943030"
---
# <span data-ttu-id="b4df7-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="b4df7-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="b4df7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4df7-102">SYNOPSIS</span></span>
<span data-ttu-id="b4df7-103">Desativar o salvamento de credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4df7-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="b4df7-104">Suas informações de login serão esquecidas na próxima vez que você abrir uma janela do PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4df7-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="b4df7-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4df7-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4df7-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4df7-106">DESCRIPTION</span></span>
<span data-ttu-id="b4df7-107">Desativar o salvamento de credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4df7-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="b4df7-108">Suas informações de login serão esquecidas na próxima vez que você abrir uma janela do PowerShell</span><span class="sxs-lookup"><span data-stu-id="b4df7-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="b4df7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4df7-109">EXAMPLES</span></span>

### <span data-ttu-id="b4df7-110">Desabilitar o salvamento AutoTexto</span><span class="sxs-lookup"><span data-stu-id="b4df7-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="b4df7-111">Desabilitar o salvamento automático do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="b4df7-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="b4df7-112">OS</span><span class="sxs-lookup"><span data-stu-id="b4df7-112">PARAMETERS</span></span>

### <span data-ttu-id="b4df7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4df7-113">-DefaultProfile</span></span>
<span data-ttu-id="b4df7-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b4df7-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4df7-115">-Escopo</span><span class="sxs-lookup"><span data-stu-id="b4df7-115">-Scope</span></span>
<span data-ttu-id="b4df7-116">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="b4df7-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="b4df7-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4df7-117">-Confirm</span></span>
<span data-ttu-id="b4df7-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4df7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4df7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4df7-119">-WhatIf</span></span>
<span data-ttu-id="b4df7-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4df7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4df7-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4df7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4df7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4df7-122">CommonParameters</span></span>
<span data-ttu-id="b4df7-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4df7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4df7-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4df7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4df7-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4df7-125">INPUTS</span></span>

### <span data-ttu-id="b4df7-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b4df7-126">None</span></span>

## <span data-ttu-id="b4df7-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4df7-127">OUTPUTS</span></span>

### <span data-ttu-id="b4df7-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="b4df7-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="b4df7-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4df7-129">NOTES</span></span>

## <span data-ttu-id="b4df7-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4df7-130">RELATED LINKS</span></span>
