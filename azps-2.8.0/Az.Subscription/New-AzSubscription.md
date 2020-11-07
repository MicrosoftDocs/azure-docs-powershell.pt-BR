---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
ms.openlocfilehash: e26465e2d307b55690a5aef7ffae81abbe9edc40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774264"
---
# <span data-ttu-id="5eb52-101">New-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="5eb52-101">New-AzSubscription</span></span>

## <span data-ttu-id="5eb52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5eb52-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb52-103">Cria uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb52-103">Creates an Azure subscription.</span></span>

## <span data-ttu-id="5eb52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5eb52-104">SYNTAX</span></span>

```
New-AzSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eb52-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5eb52-105">DESCRIPTION</span></span>
<span data-ttu-id="5eb52-106">O cmdlet **New-AzSubscription** cria uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb52-106">The **New-AzSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="5eb52-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5eb52-107">EXAMPLES</span></span>

### <span data-ttu-id="5eb52-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5eb52-108">Example 1</span></span>
```
PS C:\> New-AzSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="5eb52-109">Cria uma assinatura do Azure na conta de registro especificada com o tipo de oferta especificado.</span><span class="sxs-lookup"><span data-stu-id="5eb52-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="5eb52-110">OS</span><span class="sxs-lookup"><span data-stu-id="5eb52-110">PARAMETERS</span></span>

### <span data-ttu-id="5eb52-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5eb52-111">-AsJob</span></span>
<span data-ttu-id="5eb52-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5eb52-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5eb52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb52-113">-DefaultProfile</span></span>
<span data-ttu-id="5eb52-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb52-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eb52-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="5eb52-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="5eb52-116">Nome da conta de registro a ser usada ao criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="5eb52-116">Name of the enrollment account to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb52-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5eb52-117">-Name</span></span>
<span data-ttu-id="5eb52-118">O nome da assinatura a ser criada.</span><span class="sxs-lookup"><span data-stu-id="5eb52-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb52-119">-Offertype</span><span class="sxs-lookup"><span data-stu-id="5eb52-119">-OfferType</span></span>
<span data-ttu-id="5eb52-120">O tipo de oferta a ser usado ao criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="5eb52-120">The type of offer to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb52-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="5eb52-121">-OwnerApplicationId</span></span>
<span data-ttu-id="5eb52-122">O (s) SPN (s) do aplicativo a ser concedido acesso à assinatura.</span><span class="sxs-lookup"><span data-stu-id="5eb52-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb52-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="5eb52-123">-OwnerObjectId</span></span>
<span data-ttu-id="5eb52-124">O (s) usuário (s) ou a (s) ID (s) do (s) objeto (s) de grupo a (s) conceder acesso à assinatura.</span><span class="sxs-lookup"><span data-stu-id="5eb52-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb52-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="5eb52-125">-OwnerSignInName</span></span>
<span data-ttu-id="5eb52-126">O (s) usuário (s) conceder acesso de proprietário à assinatura.</span><span class="sxs-lookup"><span data-stu-id="5eb52-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb52-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5eb52-127">-Confirm</span></span>
<span data-ttu-id="5eb52-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eb52-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eb52-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb52-129">-WhatIf</span></span>
<span data-ttu-id="5eb52-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5eb52-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5eb52-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5eb52-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eb52-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb52-132">CommonParameters</span></span>
<span data-ttu-id="5eb52-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb52-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb52-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eb52-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb52-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5eb52-135">INPUTS</span></span>

### <span data-ttu-id="5eb52-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5eb52-136">None</span></span>

## <span data-ttu-id="5eb52-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5eb52-137">OUTPUTS</span></span>

### <span data-ttu-id="5eb52-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="5eb52-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="5eb52-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5eb52-139">NOTES</span></span>

## <span data-ttu-id="5eb52-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eb52-140">RELATED LINKS</span></span>
