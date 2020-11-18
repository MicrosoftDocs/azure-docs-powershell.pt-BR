---
title: Gerenciar assinaturas do Azure com o Azure PowerShell
description: Gerenciar assinaturas do Azure com o Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 4f48e009d9769cba671ea54e8f619a9ad40603d1
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715112"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="91b97-103">Usar várias assinaturas do Azure</span><span class="sxs-lookup"><span data-stu-id="91b97-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="91b97-104">A maioria dos usuários do Azure terá somente uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="91b97-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="91b97-105">No entanto, se você fizer parte de mais de uma organização ou se sua organização tiver dividido o acesso a determinados recursos nos agrupamentos, poderá ter várias assinaturas no Azure.</span><span class="sxs-lookup"><span data-stu-id="91b97-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="91b97-106">A CLI é compatível com a escolha de uma assinatura globalmente e por comando.</span><span class="sxs-lookup"><span data-stu-id="91b97-106">The CLI supports selecting a subscription both globally and per command.</span></span>

<span data-ttu-id="91b97-107">Para obter informações detalhadas sobre assinaturas, cobrança e gerenciamento de custos, confira a [documentação sobre cobrança e gerenciamento de custos](/azure/billing/).</span><span class="sxs-lookup"><span data-stu-id="91b97-107">For detailed information on subscriptions, billing, and cost management, see the [billing and cost management documentation](/azure/billing/).</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="91b97-108">Locatários, usuários e assinaturas</span><span class="sxs-lookup"><span data-stu-id="91b97-108">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="91b97-109">Talvez você tenha alguma confusão sobre a diferença entre locatários, usuários e assinaturas no Azure.</span><span class="sxs-lookup"><span data-stu-id="91b97-109">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="91b97-110">Um _locatário_ é a entidade do Azure Active Directory que abrange toda a organização.</span><span class="sxs-lookup"><span data-stu-id="91b97-110">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="91b97-111">Esse locatário tem pelo menos uma _assinatura_ e _usuário_.</span><span class="sxs-lookup"><span data-stu-id="91b97-111">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="91b97-112">Um usuário é um indivíduo e é associado a somente um locatário: a organização à qual pertence.</span><span class="sxs-lookup"><span data-stu-id="91b97-112">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="91b97-113">Os usuários são as contas que se conectam ao Azure para criar, gerenciar e usar recursos.</span><span class="sxs-lookup"><span data-stu-id="91b97-113">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="91b97-114">Um usuário pode ter acesso a várias _assinaturas_, que são contratos com a Microsoft para usar os serviços de nuvem, incluindo o Azure.</span><span class="sxs-lookup"><span data-stu-id="91b97-114">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="91b97-115">Cada recurso é associado a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="91b97-115">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="91b97-116">Para saber mais sobre as diferenças entre locatários, usuários e assinaturas, confira o [dicionário de terminologia de nuvem do Azure](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="91b97-116">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="91b97-117">Para saber como adicionar uma nova assinatura ao seu locatário do Azure Active Directory, confira [Como associar ou adicionar uma assinatura do Azure ao locatário do Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="91b97-117">To learn how to add a new subscription to your Azure Active Directory tenant, see [Associate or add an Azure subscription to your Azure Active Directory tenant](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="91b97-118">Para saber como se conectar a um locatário específico, confira [Entrar com o Azure PowerShell](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="91b97-118">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="91b97-119">Alterar a assinatura ativa</span><span class="sxs-lookup"><span data-stu-id="91b97-119">Change the active subscription</span></span>

<span data-ttu-id="91b97-120">No Azure PowerShell, para acessar os recursos de uma assinatura é preciso alterar a assinatura associada à sessão atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="91b97-120">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="91b97-121">Isso é feito modificando o contexto da sessão ativa, as informações com base nas quais os cmdlets de locatário, a assinatura e o usuário devem ser executados.</span><span class="sxs-lookup"><span data-stu-id="91b97-121">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="91b97-122">Para alterar as assinaturas, primeiro um objeto de contexto do Azure PowerShell precisa ser recuperado com [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e, em seguida, o contexto atual é alterado com [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="91b97-122">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="91b97-123">O exemplo a seguir mostra como obter uma assinatura no locatário do Active Directory atual e defini-lo como a sessão ativa:</span><span class="sxs-lookup"><span data-stu-id="91b97-123">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="91b97-124">Para saber mais sobre os contextos do Azure PowerShell, incluindo como salvá-los e alternar rapidamente entre eles para trabalhar com várias assinaturas com facilidade, confira [Persistir credenciais com contextos do Azure PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="91b97-124">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>
