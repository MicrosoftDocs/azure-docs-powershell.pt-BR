---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112430"
---
# <span data-ttu-id="134f7-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="134f7-101">Update-AzSubscription</span></span>

## <span data-ttu-id="134f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="134f7-102">SYNOPSIS</span></span>
<span data-ttu-id="134f7-103">Atualiza uma assinatura do Azure</span><span class="sxs-lookup"><span data-stu-id="134f7-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="134f7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="134f7-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="134f7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="134f7-105">DESCRIPTION</span></span>
<span data-ttu-id="134f7-106">O cmdlet **Update-AzSubscription** atualiza uma assinatura do Azure</span><span class="sxs-lookup"><span data-stu-id="134f7-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="134f7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="134f7-107">EXAMPLES</span></span>

### <span data-ttu-id="134f7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="134f7-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="134f7-109">Atualiza a assinatura</span><span class="sxs-lookup"><span data-stu-id="134f7-109">Updates the subscription</span></span>

## <span data-ttu-id="134f7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="134f7-110">PARAMETERS</span></span>

### <span data-ttu-id="134f7-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="134f7-111">-Action</span></span>
<span data-ttu-id="134f7-112">Ação a ser executar na assinatura</span><span class="sxs-lookup"><span data-stu-id="134f7-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="134f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="134f7-113">-AsJob</span></span>
<span data-ttu-id="134f7-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="134f7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="134f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134f7-115">-DefaultProfile</span></span>
<span data-ttu-id="134f7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="134f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="134f7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="134f7-117">-Name</span></span>
<span data-ttu-id="134f7-118">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="134f7-118">Name of the subscription</span></span>

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

### <span data-ttu-id="134f7-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="134f7-119">-SubscriptionId</span></span>
<span data-ttu-id="134f7-120">ID da assinatura para atualizar</span><span class="sxs-lookup"><span data-stu-id="134f7-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="134f7-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="134f7-121">-Confirm</span></span>
<span data-ttu-id="134f7-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="134f7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="134f7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="134f7-123">-WhatIf</span></span>
<span data-ttu-id="134f7-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="134f7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="134f7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="134f7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="134f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134f7-126">CommonParameters</span></span>
<span data-ttu-id="134f7-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="134f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134f7-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="134f7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134f7-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="134f7-129">INPUTS</span></span>

### <span data-ttu-id="134f7-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="134f7-130">None</span></span>

## <span data-ttu-id="134f7-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="134f7-131">OUTPUTS</span></span>

### <span data-ttu-id="134f7-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="134f7-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="134f7-133">Notas</span><span class="sxs-lookup"><span data-stu-id="134f7-133">NOTES</span></span>

## <span data-ttu-id="134f7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="134f7-134">RELATED LINKS</span></span>
