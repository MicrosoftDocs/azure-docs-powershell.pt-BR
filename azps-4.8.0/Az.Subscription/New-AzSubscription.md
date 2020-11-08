---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
ms.openlocfilehash: 167678bfe84117cdc53e9e90b520abe24fed4b92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111246"
---
# <span data-ttu-id="b9e15-101">New-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="b9e15-101">New-AzSubscription</span></span>

## <span data-ttu-id="b9e15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9e15-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e15-103">Cria uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e15-103">Creates an Azure subscription.</span></span>

## <span data-ttu-id="b9e15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9e15-104">SYNTAX</span></span>

```
New-AzSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e15-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9e15-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e15-106">O cmdlet **New-AzSubscription** cria uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e15-106">The **New-AzSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="b9e15-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9e15-107">EXAMPLES</span></span>

### <span data-ttu-id="b9e15-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9e15-108">Example 1</span></span>
```
PS C:\> New-AzSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="b9e15-109">Cria uma assinatura do Azure na conta de registro especificada com o tipo de oferta especificado.</span><span class="sxs-lookup"><span data-stu-id="b9e15-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="b9e15-110">OS</span><span class="sxs-lookup"><span data-stu-id="b9e15-110">PARAMETERS</span></span>

### <span data-ttu-id="b9e15-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9e15-111">-AsJob</span></span>
<span data-ttu-id="b9e15-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b9e15-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9e15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e15-113">-DefaultProfile</span></span>
<span data-ttu-id="b9e15-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e15-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9e15-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="b9e15-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="b9e15-116">Nome da conta de registro a ser usada ao criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9e15-116">Name of the enrollment account to use when creating the subscription.</span></span>

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

### <span data-ttu-id="b9e15-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9e15-117">-Name</span></span>
<span data-ttu-id="b9e15-118">O nome da assinatura a ser criada.</span><span class="sxs-lookup"><span data-stu-id="b9e15-118">The name of the subscription to create.</span></span>

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

### <span data-ttu-id="b9e15-119">-Offertype</span><span class="sxs-lookup"><span data-stu-id="b9e15-119">-OfferType</span></span>
<span data-ttu-id="b9e15-120">O tipo de oferta a ser usado ao criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9e15-120">The type of offer to use when creating the subscription.</span></span>

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

### <span data-ttu-id="b9e15-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="b9e15-121">-OwnerApplicationId</span></span>
<span data-ttu-id="b9e15-122">O (s) SPN (s) do aplicativo a ser concedido acesso à assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9e15-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

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

### <span data-ttu-id="b9e15-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="b9e15-123">-OwnerObjectId</span></span>
<span data-ttu-id="b9e15-124">O (s) usuário (s) ou a (s) ID (s) do (s) objeto (s) de grupo a (s) conceder acesso à assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9e15-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

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

### <span data-ttu-id="b9e15-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="b9e15-125">-OwnerSignInName</span></span>
<span data-ttu-id="b9e15-126">O (s) usuário (s) conceder acesso de proprietário à assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9e15-126">The user(s) to be granted Owner access to the subscription.</span></span>

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

### <span data-ttu-id="b9e15-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9e15-127">-Confirm</span></span>
<span data-ttu-id="b9e15-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9e15-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e15-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e15-129">-WhatIf</span></span>
<span data-ttu-id="b9e15-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9e15-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9e15-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9e15-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e15-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e15-132">CommonParameters</span></span>
<span data-ttu-id="b9e15-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e15-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e15-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e15-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e15-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9e15-135">INPUTS</span></span>

### <span data-ttu-id="b9e15-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b9e15-136">None</span></span>

## <span data-ttu-id="b9e15-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9e15-137">OUTPUTS</span></span>

### <span data-ttu-id="b9e15-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b9e15-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="b9e15-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9e15-139">NOTES</span></span>

## <span data-ttu-id="b9e15-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9e15-140">RELATED LINKS</span></span>
