---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 96b9b5a6bec10082d7b004dcede73b743a7e538b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439850"
---
# <span data-ttu-id="e4391-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e4391-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="e4391-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4391-102">SYNOPSIS</span></span>
<span data-ttu-id="e4391-103">Obtém os metadados usados para autenticar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e4391-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4391-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4391-104">SYNTAX</span></span>

### <span data-ttu-id="e4391-105">GetSingleContext (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4391-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="e4391-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="e4391-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4391-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4391-107">DESCRIPTION</span></span>
<span data-ttu-id="e4391-108">O cmdlet Get-AzureRmContext Obtém os metadados atuais usados para autenticar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e4391-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="e4391-109">Esse cmdlet obtém a conta do Active Directory, o locatário do Active Directory, a assinatura do Azure e o ambiente de destino do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4391-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="e4391-110">Os cmdlets do Azure Resource Manager usam essas configurações por padrão ao realizar solicitações do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e4391-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="e4391-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4391-111">EXAMPLES</span></span>

### <span data-ttu-id="e4391-112">Exemplo 1: obtendo o contexto atual</span><span class="sxs-lookup"><span data-stu-id="e4391-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="e4391-113">Neste exemplo, estamos nos conectando à nossa conta com uma assinatura do Azure usando Connect-AzureRmAccount e estamos obtendo o contexto da sessão atual chamando Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="e4391-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="e4391-114">Exemplo 2: listando todos os contextos disponíveis</span><span class="sxs-lookup"><span data-stu-id="e4391-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

<span data-ttu-id="e4391-115">Neste exemplo, todos os contextos disponíveis no momento são exibidos.</span><span class="sxs-lookup"><span data-stu-id="e4391-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="e4391-116">O usuário pode selecionar um desses contextos usando Select-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="e4391-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="e4391-117">OS</span><span class="sxs-lookup"><span data-stu-id="e4391-117">PARAMETERS</span></span>

### <span data-ttu-id="e4391-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4391-118">-DefaultProfile</span></span>
<span data-ttu-id="e4391-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e4391-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4391-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="e4391-120">-ListAvailable</span></span>
<span data-ttu-id="e4391-121">Listar todos os contextos disponíveis na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="e4391-121">List all available contexts in the current session.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4391-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4391-122">-Name</span></span>
<span data-ttu-id="e4391-123">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="e4391-123">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4391-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4391-124">CommonParameters</span></span>
<span data-ttu-id="e4391-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4391-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4391-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4391-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4391-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4391-127">INPUTS</span></span>

### <span data-ttu-id="e4391-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e4391-128">None</span></span>
<span data-ttu-id="e4391-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e4391-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4391-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4391-130">OUTPUTS</span></span>

### <span data-ttu-id="e4391-131">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="e4391-131">PSAzureContext</span></span>
<span data-ttu-id="e4391-132">Esse cmdlet retorna a conta, o locatário e a assinatura usadas pelos cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e4391-132">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="e4391-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4391-133">NOTES</span></span>

## <span data-ttu-id="e4391-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4391-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4391-135">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="e4391-135">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

