---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112437"
---
# <span data-ttu-id="1a304-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="1a304-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="1a304-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a304-102">SYNOPSIS</span></span>
<span data-ttu-id="1a304-103">Obtém detalhes do alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="1a304-103">Gets subscription alias details</span></span>

## <span data-ttu-id="1a304-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a304-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a304-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a304-105">DESCRIPTION</span></span>
<span data-ttu-id="1a304-106">O cmdlet **Get-AzSubscriptionAlias** obtém detalhes de alias de assinatura.</span><span class="sxs-lookup"><span data-stu-id="1a304-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="1a304-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a304-107">EXAMPLES</span></span>

### <span data-ttu-id="1a304-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1a304-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="1a304-109">Obtém detalhes do alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="1a304-109">Gets subscription alias details</span></span>

## <span data-ttu-id="1a304-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a304-110">PARAMETERS</span></span>

### <span data-ttu-id="1a304-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="1a304-111">-AliasName</span></span>
<span data-ttu-id="1a304-112">Alias da assinatura</span><span class="sxs-lookup"><span data-stu-id="1a304-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="1a304-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a304-113">-AsJob</span></span>
<span data-ttu-id="1a304-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1a304-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a304-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a304-115">-DefaultProfile</span></span>
<span data-ttu-id="1a304-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a304-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a304-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1a304-117">-Confirm</span></span>
<span data-ttu-id="1a304-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a304-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a304-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a304-119">-WhatIf</span></span>
<span data-ttu-id="1a304-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1a304-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a304-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a304-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a304-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a304-122">CommonParameters</span></span>
<span data-ttu-id="1a304-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a304-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a304-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a304-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a304-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="1a304-125">INPUTS</span></span>

### <span data-ttu-id="1a304-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1a304-126">None</span></span>

## <span data-ttu-id="1a304-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="1a304-127">OUTPUTS</span></span>

### <span data-ttu-id="1a304-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="1a304-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="1a304-129">Notas</span><span class="sxs-lookup"><span data-stu-id="1a304-129">NOTES</span></span>

## <span data-ttu-id="1a304-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a304-130">RELATED LINKS</span></span>
