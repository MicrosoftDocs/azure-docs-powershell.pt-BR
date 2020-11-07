---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 9dcf7b7d7149235d5a2ed211dbccf87415f1c496
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775193"
---
# <span data-ttu-id="fc502-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="fc502-101">Clear-AzContext</span></span>

## <span data-ttu-id="fc502-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc502-102">SYNOPSIS</span></span>
<span data-ttu-id="fc502-103">Remova todas as credenciais do Azure, conta e informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="fc502-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="fc502-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc502-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc502-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc502-105">DESCRIPTION</span></span>
<span data-ttu-id="fc502-106">Remova todas as credenciais do Azure, conta e informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="fc502-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="fc502-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc502-107">EXAMPLES</span></span>

### <span data-ttu-id="fc502-108">Limpar contexto global</span><span class="sxs-lookup"><span data-stu-id="fc502-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="fc502-109">Remova todas as informações de conta, assinatura e credenciais para qualquer sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc502-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="fc502-110">OS</span><span class="sxs-lookup"><span data-stu-id="fc502-110">PARAMETERS</span></span>

### <span data-ttu-id="fc502-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc502-111">-DefaultProfile</span></span>
<span data-ttu-id="fc502-112">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fc502-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc502-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fc502-113">-Force</span></span>
<span data-ttu-id="fc502-114">Excluir todos os usuários e grupos do escopo global sem solicitação</span><span class="sxs-lookup"><span data-stu-id="fc502-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="fc502-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc502-115">-PassThru</span></span>
<span data-ttu-id="fc502-116">Retornar um valor que indica êxito ou falha</span><span class="sxs-lookup"><span data-stu-id="fc502-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="fc502-117">-Escopo</span><span class="sxs-lookup"><span data-stu-id="fc502-117">-Scope</span></span>
<span data-ttu-id="fc502-118">Limpe o contexto somente para a sessão atual do PowerShell ou para todas as sessões.</span><span class="sxs-lookup"><span data-stu-id="fc502-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="fc502-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc502-119">-Confirm</span></span>
<span data-ttu-id="fc502-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc502-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc502-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc502-121">-WhatIf</span></span>
<span data-ttu-id="fc502-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc502-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc502-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc502-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc502-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc502-124">CommonParameters</span></span>
<span data-ttu-id="fc502-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc502-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc502-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc502-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc502-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc502-127">INPUTS</span></span>

### <span data-ttu-id="fc502-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fc502-128">None</span></span>

## <span data-ttu-id="fc502-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc502-129">OUTPUTS</span></span>

### <span data-ttu-id="fc502-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc502-130">System.Boolean</span></span>

## <span data-ttu-id="fc502-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc502-131">NOTES</span></span>

## <span data-ttu-id="fc502-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc502-132">RELATED LINKS</span></span>
