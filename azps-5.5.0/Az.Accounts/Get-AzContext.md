---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111248"
---
# <span data-ttu-id="26a75-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="26a75-101">Get-AzContext</span></span>

## <span data-ttu-id="26a75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26a75-102">SYNOPSIS</span></span>
<span data-ttu-id="26a75-103">Obtém os metadados usados para autenticar as solicitações do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="26a75-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="26a75-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26a75-104">SYNTAX</span></span>

### <span data-ttu-id="26a75-105">GetSingleContext (Padrão)</span><span class="sxs-lookup"><span data-stu-id="26a75-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="26a75-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="26a75-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26a75-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="26a75-107">DESCRIPTION</span></span>
<span data-ttu-id="26a75-108">O Get-AzContext cmdlet obtém os metadados atuais usados para autenticar as solicitações do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="26a75-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="26a75-109">Este cmdlet obtém a conta do Active Directory, o locatário do Active Directory, a assinatura do Azure e o ambiente direcionado do Azure.</span><span class="sxs-lookup"><span data-stu-id="26a75-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="26a75-110">Os cmdlets do Gerenciador de Recursos do Azure usam essas configurações por padrão ao fazer solicitações do Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="26a75-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="26a75-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="26a75-111">EXAMPLES</span></span>

### <span data-ttu-id="26a75-112">Exemplo 1: Obter o contexto atual</span><span class="sxs-lookup"><span data-stu-id="26a75-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="26a75-113">Neste exemplo, estamos entrando em nossa conta com uma assinatura do Azure usando Connect-AzAccount e, em seguida, estamos recebendo o contexto da sessão atual chamando Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="26a75-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="26a75-114">Exemplo 2: Listando todos os contextos disponíveis</span><span class="sxs-lookup"><span data-stu-id="26a75-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="26a75-115">Neste exemplo, todos os contextos disponíveis no momento são exibidos.</span><span class="sxs-lookup"><span data-stu-id="26a75-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="26a75-116">O usuário pode selecionar um desses contextos usando Select-AzContext.</span><span class="sxs-lookup"><span data-stu-id="26a75-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="26a75-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26a75-117">PARAMETERS</span></span>

### <span data-ttu-id="26a75-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a75-118">-DefaultProfile</span></span>
<span data-ttu-id="26a75-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="26a75-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26a75-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="26a75-120">-ListAvailable</span></span>
<span data-ttu-id="26a75-121">Listar todos os contextos disponíveis na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="26a75-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="26a75-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="26a75-122">-Name</span></span>
<span data-ttu-id="26a75-123">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="26a75-123">The name of the context</span></span>

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

### <span data-ttu-id="26a75-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a75-124">CommonParameters</span></span>
<span data-ttu-id="26a75-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a75-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a75-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26a75-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a75-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="26a75-127">INPUTS</span></span>

### <span data-ttu-id="26a75-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="26a75-128">None</span></span>

## <span data-ttu-id="26a75-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="26a75-129">OUTPUTS</span></span>

### <span data-ttu-id="26a75-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="26a75-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="26a75-131">Notas</span><span class="sxs-lookup"><span data-stu-id="26a75-131">NOTES</span></span>

## <span data-ttu-id="26a75-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26a75-132">RELATED LINKS</span></span>

[<span data-ttu-id="26a75-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="26a75-133">Set-AzContext</span></span>](./Set-AzContext.md)

