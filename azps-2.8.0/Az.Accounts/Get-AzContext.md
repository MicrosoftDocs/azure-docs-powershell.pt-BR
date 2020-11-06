---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 0f306b7e42dbe5b37c1c814a9458a5e1fb81cc7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598261"
---
# <span data-ttu-id="7805b-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="7805b-101">Get-AzContext</span></span>

## <span data-ttu-id="7805b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7805b-102">SYNOPSIS</span></span>
<span data-ttu-id="7805b-103">Obtém os metadados usados para autenticar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7805b-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="7805b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7805b-104">SYNTAX</span></span>

### <span data-ttu-id="7805b-105">GetSingleContext (padrão)</span><span class="sxs-lookup"><span data-stu-id="7805b-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="7805b-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="7805b-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7805b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7805b-107">DESCRIPTION</span></span>
<span data-ttu-id="7805b-108">O cmdlet Get-AzContext Obtém os metadados atuais usados para autenticar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7805b-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="7805b-109">Esse cmdlet obtém a conta do Active Directory, o locatário do Active Directory, a assinatura do Azure e o ambiente de destino do Azure.</span><span class="sxs-lookup"><span data-stu-id="7805b-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="7805b-110">Os cmdlets do Azure Resource Manager usam essas configurações por padrão ao realizar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7805b-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="7805b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7805b-111">EXAMPLES</span></span>

### <span data-ttu-id="7805b-112">Exemplo 1: obtendo o contexto atual</span><span class="sxs-lookup"><span data-stu-id="7805b-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="7805b-113">Neste exemplo, estamos nos conectando à nossa conta com uma assinatura do Azure usando Connect-AzAccount e estamos obtendo o contexto da sessão atual chamando Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="7805b-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="7805b-114">Exemplo 2: listando todos os contextos disponíveis</span><span class="sxs-lookup"><span data-stu-id="7805b-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="7805b-115">Neste exemplo, todos os contextos disponíveis no momento são exibidos.</span><span class="sxs-lookup"><span data-stu-id="7805b-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="7805b-116">O usuário pode selecionar um desses contextos usando Select-AzContext.</span><span class="sxs-lookup"><span data-stu-id="7805b-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="7805b-117">OS</span><span class="sxs-lookup"><span data-stu-id="7805b-117">PARAMETERS</span></span>

### <span data-ttu-id="7805b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7805b-118">-DefaultProfile</span></span>
<span data-ttu-id="7805b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7805b-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7805b-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="7805b-120">-ListAvailable</span></span>
<span data-ttu-id="7805b-121">Listar todos os contextos disponíveis na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="7805b-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="7805b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7805b-122">-Name</span></span>
<span data-ttu-id="7805b-123">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="7805b-123">The name of the context</span></span>

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

### <span data-ttu-id="7805b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7805b-124">CommonParameters</span></span>
<span data-ttu-id="7805b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7805b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7805b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7805b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7805b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7805b-127">INPUTS</span></span>

### <span data-ttu-id="7805b-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7805b-128">None</span></span>

## <span data-ttu-id="7805b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7805b-129">OUTPUTS</span></span>

### <span data-ttu-id="7805b-130">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="7805b-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="7805b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7805b-131">NOTES</span></span>

## <span data-ttu-id="7805b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7805b-132">RELATED LINKS</span></span>

[<span data-ttu-id="7805b-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="7805b-133">Set-AzContext</span></span>](./Set-AzContext.md)

