---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117978"
---
# <span data-ttu-id="890ab-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="890ab-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="890ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="890ab-102">SYNOPSIS</span></span>
<span data-ttu-id="890ab-103">Obtém detalhes do alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="890ab-103">Gets subscription alias details</span></span>

## <span data-ttu-id="890ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="890ab-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="890ab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="890ab-105">DESCRIPTION</span></span>
<span data-ttu-id="890ab-106">O cmdlet **Get-AzSubscriptionAlias** Obtém detalhes do alias da assinatura.</span><span class="sxs-lookup"><span data-stu-id="890ab-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="890ab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="890ab-107">EXAMPLES</span></span>

### <span data-ttu-id="890ab-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="890ab-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="890ab-109">Obtém detalhes do alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="890ab-109">Gets subscription alias details</span></span>

## <span data-ttu-id="890ab-110">OS</span><span class="sxs-lookup"><span data-stu-id="890ab-110">PARAMETERS</span></span>

### <span data-ttu-id="890ab-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="890ab-111">-AliasName</span></span>
<span data-ttu-id="890ab-112">Alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="890ab-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="890ab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="890ab-113">-AsJob</span></span>
<span data-ttu-id="890ab-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="890ab-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="890ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890ab-115">-DefaultProfile</span></span>
<span data-ttu-id="890ab-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="890ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="890ab-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="890ab-117">-Confirm</span></span>
<span data-ttu-id="890ab-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="890ab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="890ab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="890ab-119">-WhatIf</span></span>
<span data-ttu-id="890ab-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="890ab-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="890ab-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="890ab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="890ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890ab-122">CommonParameters</span></span>
<span data-ttu-id="890ab-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890ab-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="890ab-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890ab-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="890ab-125">INPUTS</span></span>

### <span data-ttu-id="890ab-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="890ab-126">None</span></span>

## <span data-ttu-id="890ab-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="890ab-127">OUTPUTS</span></span>

### <span data-ttu-id="890ab-128">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="890ab-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="890ab-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="890ab-129">NOTES</span></span>

## <span data-ttu-id="890ab-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="890ab-130">RELATED LINKS</span></span>
