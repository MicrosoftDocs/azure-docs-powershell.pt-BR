---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: e56452d14f9c0f17b4f744d08fdd5911fb39aff5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775261"
---
# <span data-ttu-id="8e28e-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="8e28e-101">Get-AzContext</span></span>

## <span data-ttu-id="8e28e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e28e-102">SYNOPSIS</span></span>
<span data-ttu-id="8e28e-103">Obtém os metadados usados para autenticar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8e28e-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="8e28e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e28e-104">SYNTAX</span></span>

### <span data-ttu-id="8e28e-105">GetSingleContext (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e28e-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="8e28e-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="8e28e-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-RefreshContextFromTokenCache] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e28e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e28e-107">DESCRIPTION</span></span>
<span data-ttu-id="8e28e-108">O cmdlet Get-AzContext Obtém os metadados atuais usados para autenticar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8e28e-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="8e28e-109">Esse cmdlet obtém a conta do Active Directory, o locatário do Active Directory, a assinatura do Azure e o ambiente de destino do Azure.</span><span class="sxs-lookup"><span data-stu-id="8e28e-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="8e28e-110">Os cmdlets do Azure Resource Manager usam essas configurações por padrão ao realizar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8e28e-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="8e28e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e28e-111">EXAMPLES</span></span>

### <span data-ttu-id="8e28e-112">Exemplo 1: obtendo o contexto atual</span><span class="sxs-lookup"><span data-stu-id="8e28e-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="8e28e-113">Neste exemplo, estamos nos conectando à nossa conta com uma assinatura do Azure usando Connect-AzAccount e estamos obtendo o contexto da sessão atual chamando Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="8e28e-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="8e28e-114">Exemplo 2: listando todos os contextos disponíveis</span><span class="sxs-lookup"><span data-stu-id="8e28e-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="8e28e-115">Neste exemplo, todos os contextos disponíveis no momento são exibidos.</span><span class="sxs-lookup"><span data-stu-id="8e28e-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="8e28e-116">O usuário pode selecionar um desses contextos usando Select-AzContext.</span><span class="sxs-lookup"><span data-stu-id="8e28e-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="8e28e-117">OS</span><span class="sxs-lookup"><span data-stu-id="8e28e-117">PARAMETERS</span></span>

### <span data-ttu-id="8e28e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e28e-118">-DefaultProfile</span></span>
<span data-ttu-id="8e28e-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8e28e-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e28e-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="8e28e-120">-ListAvailable</span></span>
<span data-ttu-id="8e28e-121">Listar todos os contextos disponíveis na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="8e28e-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="8e28e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e28e-122">-Name</span></span>
<span data-ttu-id="8e28e-123">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="8e28e-123">The name of the context</span></span>

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

### <span data-ttu-id="8e28e-124">-RefreshContextFromTokenCache</span><span class="sxs-lookup"><span data-stu-id="8e28e-124">-RefreshContextFromTokenCache</span></span>
<span data-ttu-id="8e28e-125">Atualizar contextos do cache de token</span><span class="sxs-lookup"><span data-stu-id="8e28e-125">Refresh contexts from token cache</span></span>

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

### <span data-ttu-id="8e28e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e28e-126">CommonParameters</span></span>
<span data-ttu-id="8e28e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e28e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e28e-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e28e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e28e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e28e-129">INPUTS</span></span>

### <span data-ttu-id="8e28e-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8e28e-130">None</span></span>

## <span data-ttu-id="8e28e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e28e-131">OUTPUTS</span></span>

### <span data-ttu-id="8e28e-132">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="8e28e-132">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="8e28e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e28e-133">NOTES</span></span>

## <span data-ttu-id="8e28e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e28e-134">RELATED LINKS</span></span>

[<span data-ttu-id="8e28e-135">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="8e28e-135">Set-AzContext</span></span>](./Set-AzContext.md)

