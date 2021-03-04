---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 2060a1cbe9f002a20b94e82ac9547c5fc96c0e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892918"
---
# <span data-ttu-id="b9e7a-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="b9e7a-101">Get-AzContext</span></span>

## <span data-ttu-id="b9e7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e7a-103">Obtém os metadados usados para autenticar solicitações do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e7a-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="b9e7a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b9e7a-104">SYNTAX</span></span>

### <span data-ttu-id="b9e7a-105">GetSingleContext (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b9e7a-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9e7a-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="b9e7a-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-RefreshContextFromTokenCache] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9e7a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b9e7a-107">DESCRIPTION</span></span>
<span data-ttu-id="b9e7a-108">O Get-AzContext cmdlet obtém os metadados atuais usados para autenticar solicitações do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e7a-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="b9e7a-109">Este cmdlet obtém a conta do Active Directory, o locatário do Active Directory, a assinatura do Azure e o ambiente do Azure direcionado.</span><span class="sxs-lookup"><span data-stu-id="b9e7a-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="b9e7a-110">Os cmdlets do Gerenciador de Recursos do Azure usam essas configurações por padrão ao fazer solicitações do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e7a-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="b9e7a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9e7a-111">EXAMPLES</span></span>

### <span data-ttu-id="b9e7a-112">Exemplo 1: Obter o contexto atual</span><span class="sxs-lookup"><span data-stu-id="b9e7a-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="b9e7a-113">Neste exemplo, estamos fazendo logon em nossa conta com uma assinatura do Azure usando Connect-AzAccount e, em seguida, estamos recebendo o contexto da sessão atual chamando Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="b9e7a-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="b9e7a-114">Exemplo 2: Listando todos os contextos disponíveis</span><span class="sxs-lookup"><span data-stu-id="b9e7a-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="b9e7a-115">Neste exemplo, todos os contextos disponíveis no momento são exibidos.</span><span class="sxs-lookup"><span data-stu-id="b9e7a-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="b9e7a-116">O usuário pode selecionar um desses contextos usando Select-AzContext.</span><span class="sxs-lookup"><span data-stu-id="b9e7a-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="b9e7a-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b9e7a-117">PARAMETERS</span></span>

### <span data-ttu-id="b9e7a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e7a-118">-DefaultProfile</span></span>
<span data-ttu-id="b9e7a-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b9e7a-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9e7a-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b9e7a-120">-ListAvailable</span></span>
<span data-ttu-id="b9e7a-121">Listar todos os contextos disponíveis na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="b9e7a-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b9e7a-122">-Name</span></span>
<span data-ttu-id="b9e7a-123">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="b9e7a-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7a-124">-RefreshContextFromTokenCache</span><span class="sxs-lookup"><span data-stu-id="b9e7a-124">-RefreshContextFromTokenCache</span></span>
<span data-ttu-id="b9e7a-125">Atualizar contextos do cache de token</span><span class="sxs-lookup"><span data-stu-id="b9e7a-125">Refresh contexts from token cache</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e7a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e7a-126">CommonParameters</span></span>
<span data-ttu-id="b9e7a-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e7a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e7a-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9e7a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e7a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9e7a-129">INPUTS</span></span>

### <span data-ttu-id="b9e7a-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b9e7a-130">None</span></span>

## <span data-ttu-id="b9e7a-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b9e7a-131">OUTPUTS</span></span>

### <span data-ttu-id="b9e7a-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b9e7a-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="b9e7a-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="b9e7a-133">NOTES</span></span>

## <span data-ttu-id="b9e7a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9e7a-134">RELATED LINKS</span></span>

[<span data-ttu-id="b9e7a-135">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="b9e7a-135">Set-AzContext</span></span>](./Set-AzContext.md)

