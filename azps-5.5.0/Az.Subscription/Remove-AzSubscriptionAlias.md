---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112433"
---
# <span data-ttu-id="5cbf4-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="5cbf4-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="5cbf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5cbf4-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbf4-103">Exclui o alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="5cbf4-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="5cbf4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cbf4-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cbf4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cbf4-105">DESCRIPTION</span></span>
<span data-ttu-id="5cbf4-106">O cmdlet **Remove-AzSubscriptionAlias** remove o alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="5cbf4-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="5cbf4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5cbf4-107">EXAMPLES</span></span>

### <span data-ttu-id="5cbf4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5cbf4-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="5cbf4-109">Exclui o alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="5cbf4-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="5cbf4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cbf4-110">PARAMETERS</span></span>

### <span data-ttu-id="5cbf4-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="5cbf4-111">-AliasName</span></span>
<span data-ttu-id="5cbf4-112">Alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="5cbf4-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="5cbf4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cbf4-113">-AsJob</span></span>
<span data-ttu-id="5cbf4-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5cbf4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cbf4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbf4-115">-DefaultProfile</span></span>
<span data-ttu-id="5cbf4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5cbf4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cbf4-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5cbf4-117">-Confirm</span></span>
<span data-ttu-id="5cbf4-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbf4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbf4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cbf4-119">-WhatIf</span></span>
<span data-ttu-id="5cbf4-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5cbf4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cbf4-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5cbf4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbf4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbf4-122">CommonParameters</span></span>
<span data-ttu-id="5cbf4-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbf4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbf4-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cbf4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbf4-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="5cbf4-125">INPUTS</span></span>

### <span data-ttu-id="5cbf4-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5cbf4-126">None</span></span>

## <span data-ttu-id="5cbf4-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="5cbf4-127">OUTPUTS</span></span>

### <span data-ttu-id="5cbf4-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="5cbf4-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="5cbf4-129">Notas</span><span class="sxs-lookup"><span data-stu-id="5cbf4-129">NOTES</span></span>

## <span data-ttu-id="5cbf4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cbf4-130">RELATED LINKS</span></span>
