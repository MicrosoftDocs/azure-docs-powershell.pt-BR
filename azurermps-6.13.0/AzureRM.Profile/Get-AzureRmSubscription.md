---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 62f3e1b357c0a85f30ba4eeba6a92d9b8dfc9dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430095"
---
# <span data-ttu-id="9457d-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="9457d-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="9457d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9457d-102">SYNOPSIS</span></span>
<span data-ttu-id="9457d-103">Obter assinaturas que podem ser acessadas pela conta atual.</span><span class="sxs-lookup"><span data-stu-id="9457d-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9457d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9457d-104">SYNTAX</span></span>

### <span data-ttu-id="9457d-105">ListByIdInTenant (padrão)</span><span class="sxs-lookup"><span data-stu-id="9457d-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9457d-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="9457d-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9457d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9457d-107">DESCRIPTION</span></span>
<span data-ttu-id="9457d-108">O cmdlet Get-AzureRmSubscription Obtém a ID da assinatura, o nome da assinatura e o locatário doméstico para assinaturas que podem ser acessadas pela conta atual.</span><span class="sxs-lookup"><span data-stu-id="9457d-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="9457d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9457d-109">EXAMPLES</span></span>

### <span data-ttu-id="9457d-110">Exemplo 1: obter todas as assinaturas em todos os locatários</span><span class="sxs-lookup"><span data-stu-id="9457d-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="9457d-111">Esse comando obtém todas as assinaturas em todos os locatários autorizados para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="9457d-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="9457d-112">Exemplo 2: obter todas as assinaturas para um locatário específico</span><span class="sxs-lookup"><span data-stu-id="9457d-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="9457d-113">Listar todas as assinaturas no locatário especificado que são autorizadas para a conta atual.</span><span class="sxs-lookup"><span data-stu-id="9457d-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="9457d-114">Exemplo 3: obter todas as assinaturas no locatário atual</span><span class="sxs-lookup"><span data-stu-id="9457d-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="9457d-115">Esse comando obtém todas as assinaturas no locatário atual que são autorizadas para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="9457d-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="9457d-116">Exemplo 4: alterar o contexto atual para usar uma assinatura específica</span><span class="sxs-lookup"><span data-stu-id="9457d-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="9457d-117">Este comando obtém a assinatura especificada e, em seguida, define o contexto atual para usá-la.</span><span class="sxs-lookup"><span data-stu-id="9457d-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="9457d-118">Todos os cmdlets subsequentes nesta sessão usam a nova assinatura (contoso assinatura 1) por padrão.</span><span class="sxs-lookup"><span data-stu-id="9457d-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="9457d-119">OS</span><span class="sxs-lookup"><span data-stu-id="9457d-119">PARAMETERS</span></span>

### <span data-ttu-id="9457d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9457d-120">-AsJob</span></span>
<span data-ttu-id="9457d-121">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="9457d-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9457d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9457d-122">-DefaultProfile</span></span>
<span data-ttu-id="9457d-123">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9457d-123">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9457d-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9457d-124">-SubscriptionId</span></span>
<span data-ttu-id="9457d-125">Especifica a ID da assinatura a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="9457d-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9457d-126">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="9457d-126">-SubscriptionName</span></span>
<span data-ttu-id="9457d-127">Especifica o nome da assinatura a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="9457d-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9457d-128">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="9457d-128">-TenantId</span></span>
<span data-ttu-id="9457d-129">Especifica a ID do locatário que contém assinaturas a serem obtidas.</span><span class="sxs-lookup"><span data-stu-id="9457d-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9457d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9457d-130">CommonParameters</span></span>
<span data-ttu-id="9457d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9457d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9457d-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9457d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9457d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9457d-133">INPUTS</span></span>

### <span data-ttu-id="9457d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9457d-134">System.String</span></span>

## <span data-ttu-id="9457d-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9457d-135">OUTPUTS</span></span>

### <span data-ttu-id="9457d-136">Microsoft. Azure. Commands. Profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9457d-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="9457d-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9457d-137">NOTES</span></span>

## <span data-ttu-id="9457d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9457d-138">RELATED LINKS</span></span>
