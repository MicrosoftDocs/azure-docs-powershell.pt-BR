---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: b83d186089558b18cbd511cdc5d0b407a997f635
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111242"
---
# <span data-ttu-id="7bc44-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="7bc44-101">Update-AzSubscription</span></span>

## <span data-ttu-id="7bc44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bc44-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc44-103">Atualiza uma assinatura do Azure</span><span class="sxs-lookup"><span data-stu-id="7bc44-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="7bc44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bc44-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bc44-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bc44-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc44-106">O cmdlet **Update-AzSubscription** atualiza uma assinatura do Azure</span><span class="sxs-lookup"><span data-stu-id="7bc44-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="7bc44-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bc44-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc44-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7bc44-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled

```
<span data-ttu-id="7bc44-109">Atualiza a assinatura</span><span class="sxs-lookup"><span data-stu-id="7bc44-109">Updates the subscription</span></span>

## <span data-ttu-id="7bc44-110">OS</span><span class="sxs-lookup"><span data-stu-id="7bc44-110">PARAMETERS</span></span>

### <span data-ttu-id="7bc44-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="7bc44-111">-Action</span></span>
<span data-ttu-id="7bc44-112">Ação a ser executada na assinatura</span><span class="sxs-lookup"><span data-stu-id="7bc44-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="7bc44-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bc44-113">-AsJob</span></span>
<span data-ttu-id="7bc44-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7bc44-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bc44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc44-115">-DefaultProfile</span></span>
<span data-ttu-id="7bc44-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bc44-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bc44-117">-Name</span></span>
<span data-ttu-id="7bc44-118">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="7bc44-118">Name of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc44-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bc44-119">-SubscriptionId</span></span>
<span data-ttu-id="7bc44-120">ID da assinatura para atualizar</span><span class="sxs-lookup"><span data-stu-id="7bc44-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="7bc44-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7bc44-121">-Confirm</span></span>
<span data-ttu-id="7bc44-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bc44-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc44-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc44-123">-WhatIf</span></span>
<span data-ttu-id="7bc44-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7bc44-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc44-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bc44-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc44-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc44-126">CommonParameters</span></span>
<span data-ttu-id="7bc44-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc44-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc44-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bc44-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc44-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bc44-129">INPUTS</span></span>

### <span data-ttu-id="7bc44-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7bc44-130">None</span></span>

## <span data-ttu-id="7bc44-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bc44-131">OUTPUTS</span></span>

### <span data-ttu-id="7bc44-132">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="7bc44-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="7bc44-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bc44-133">NOTES</span></span>

## <span data-ttu-id="7bc44-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bc44-134">RELATED LINKS</span></span>
