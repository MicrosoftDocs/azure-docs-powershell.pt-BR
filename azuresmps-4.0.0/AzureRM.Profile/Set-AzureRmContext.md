---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425919"
---
# <span data-ttu-id="98bf1-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="98bf1-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="98bf1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="98bf1-103">Define o locatário, a assinatura e o ambiente para cmdlets a serem usados na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="98bf1-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="98bf1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98bf1-104">SYNTAX</span></span>

### <span data-ttu-id="98bf1-105">Subscriptionname (padrão)</span><span class="sxs-lookup"><span data-stu-id="98bf1-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98bf1-106">Atalho</span><span class="sxs-lookup"><span data-stu-id="98bf1-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98bf1-107">SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98bf1-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98bf1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98bf1-108">DESCRIPTION</span></span>
<span data-ttu-id="98bf1-109">O cmdlet Set-AzureRmContext define informações de autenticação para cmdlets que você executa na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="98bf1-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="98bf1-110">O contexto inclui informações de locatário, assinatura e ambiente.</span><span class="sxs-lookup"><span data-stu-id="98bf1-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="98bf1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98bf1-111">EXAMPLES</span></span>

### <span data-ttu-id="98bf1-112">Exemplo 1: definir o contexto da assinatura</span><span class="sxs-lookup"><span data-stu-id="98bf1-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="98bf1-113">Este comando define o contexto para usar a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="98bf1-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="98bf1-114">OS</span><span class="sxs-lookup"><span data-stu-id="98bf1-114">PARAMETERS</span></span>

### <span data-ttu-id="98bf1-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="98bf1-115">-Context</span></span>
<span data-ttu-id="98bf1-116">Especifica o contexto da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="98bf1-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98bf1-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98bf1-117">-SubscriptionId</span></span>
<span data-ttu-id="98bf1-118">Especifica a ID da assinatura para o contexto que este cmdlet define para a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="98bf1-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98bf1-119">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="98bf1-119">-SubscriptionName</span></span>
<span data-ttu-id="98bf1-120">Especifica o nome da assinatura para o contexto que este cmdlet define para a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="98bf1-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98bf1-121">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="98bf1-121">-TenantId</span></span>
<span data-ttu-id="98bf1-122">Especifica a ID do locatário para o contexto que este cmdlet define para a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="98bf1-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98bf1-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98bf1-123">-Confirm</span></span>
<span data-ttu-id="98bf1-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98bf1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bf1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98bf1-125">-WhatIf</span></span>
<span data-ttu-id="98bf1-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98bf1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98bf1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98bf1-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bf1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98bf1-128">CommonParameters</span></span>
<span data-ttu-id="98bf1-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98bf1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98bf1-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98bf1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98bf1-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98bf1-131">INPUTS</span></span>

## <span data-ttu-id="98bf1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98bf1-132">OUTPUTS</span></span>

### <span data-ttu-id="98bf1-133">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="98bf1-133">PSAzureContext</span></span>

## <span data-ttu-id="98bf1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98bf1-134">NOTES</span></span>

## <span data-ttu-id="98bf1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98bf1-135">RELATED LINKS</span></span>

[<span data-ttu-id="98bf1-136">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="98bf1-136">Get-AzureRMContext</span></span>]()

