---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: 6f3ff6868a34eefc9b7cd45cf371b6ef29dbf469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941998"
---
# <span data-ttu-id="7b915-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="7b915-101">Select-AzContext</span></span>

## <span data-ttu-id="7b915-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b915-102">SYNOPSIS</span></span>
<span data-ttu-id="7b915-103">Selecione uma assinatura e uma conta para direcionar nos cmdlets do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7b915-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="7b915-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b915-104">SYNTAX</span></span>

### <span data-ttu-id="7b915-105">SelectByInputObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="7b915-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b915-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="7b915-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="7b915-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b915-107">DESCRIPTION</span></span>
<span data-ttu-id="7b915-108">Selecione uma assinatura para direcionar (ou conta ou locatário) nos cmdlets do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b915-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="7b915-109">Após esse cmdlet, cmdlets futuros direcionarão o contexto selecionado.</span><span class="sxs-lookup"><span data-stu-id="7b915-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="7b915-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b915-110">EXAMPLES</span></span>

### <span data-ttu-id="7b915-111">Exemplo 1: direcionar um contexto nomeado</span><span class="sxs-lookup"><span data-stu-id="7b915-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="7b915-112">Direcione cmdlets futuros do PowerShell do Azure na conta, no locatário e na assinatura no contexto ' trabalho '.</span><span class="sxs-lookup"><span data-stu-id="7b915-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="7b915-113">OS</span><span class="sxs-lookup"><span data-stu-id="7b915-113">PARAMETERS</span></span>

### <span data-ttu-id="7b915-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b915-114">-DefaultProfile</span></span>
<span data-ttu-id="7b915-115">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7b915-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b915-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b915-116">-InputObject</span></span>
<span data-ttu-id="7b915-117">Um objeto Context, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b915-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b915-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b915-118">-Name</span></span>
<span data-ttu-id="7b915-119">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="7b915-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b915-120">-Escopo</span><span class="sxs-lookup"><span data-stu-id="7b915-120">-Scope</span></span>
<span data-ttu-id="7b915-121">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="7b915-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="7b915-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b915-122">-Confirm</span></span>
<span data-ttu-id="7b915-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b915-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b915-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b915-124">-WhatIf</span></span>
<span data-ttu-id="7b915-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b915-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b915-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b915-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b915-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b915-127">CommonParameters</span></span>
<span data-ttu-id="7b915-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b915-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b915-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b915-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b915-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b915-130">INPUTS</span></span>

### <span data-ttu-id="7b915-131">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="7b915-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="7b915-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b915-132">OUTPUTS</span></span>

### <span data-ttu-id="7b915-133">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="7b915-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="7b915-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b915-134">NOTES</span></span>

## <span data-ttu-id="7b915-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b915-135">RELATED LINKS</span></span>
