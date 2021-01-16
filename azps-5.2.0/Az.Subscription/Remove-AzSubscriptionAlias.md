---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263758"
---
# <span data-ttu-id="2372c-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="2372c-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="2372c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2372c-102">SYNOPSIS</span></span>
<span data-ttu-id="2372c-103">Exclui o alias de assinatura</span><span class="sxs-lookup"><span data-stu-id="2372c-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="2372c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2372c-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2372c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2372c-105">DESCRIPTION</span></span>
<span data-ttu-id="2372c-106">O cmdlet **Remove-AzSubscriptionAlias** remove o alias de assinatura</span><span class="sxs-lookup"><span data-stu-id="2372c-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="2372c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2372c-107">EXAMPLES</span></span>

### <span data-ttu-id="2372c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2372c-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="2372c-109">Exclui o alias de assinatura</span><span class="sxs-lookup"><span data-stu-id="2372c-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="2372c-110">OS</span><span class="sxs-lookup"><span data-stu-id="2372c-110">PARAMETERS</span></span>

### <span data-ttu-id="2372c-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="2372c-111">-AliasName</span></span>
<span data-ttu-id="2372c-112">Alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="2372c-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="2372c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2372c-113">-AsJob</span></span>
<span data-ttu-id="2372c-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2372c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2372c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2372c-115">-DefaultProfile</span></span>
<span data-ttu-id="2372c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2372c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2372c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2372c-117">-Confirm</span></span>
<span data-ttu-id="2372c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2372c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2372c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2372c-119">-WhatIf</span></span>
<span data-ttu-id="2372c-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2372c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2372c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2372c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2372c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2372c-122">CommonParameters</span></span>
<span data-ttu-id="2372c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2372c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2372c-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2372c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2372c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2372c-125">INPUTS</span></span>

### <span data-ttu-id="2372c-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2372c-126">None</span></span>

## <span data-ttu-id="2372c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2372c-127">OUTPUTS</span></span>

### <span data-ttu-id="2372c-128">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="2372c-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="2372c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2372c-129">NOTES</span></span>

## <span data-ttu-id="2372c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2372c-130">RELATED LINKS</span></span>
