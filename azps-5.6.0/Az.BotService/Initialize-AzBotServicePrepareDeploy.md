---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 118fce3e75ee7ba66fa30e6e07cfce16e5dadcff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892815"
---
# <span data-ttu-id="0a2f3-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="0a2f3-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="0a2f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2f3-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0a2f3-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="0a2f3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0a2f3-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0a2f3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0a2f3-105">DESCRIPTION</span></span>
<span data-ttu-id="0a2f3-106">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0a2f3-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="0a2f3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a2f3-107">EXAMPLES</span></span>

### <span data-ttu-id="0a2f3-108">Exemplo 1: Inicializar o Project FileFolder</span><span class="sxs-lookup"><span data-stu-id="0a2f3-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="0a2f3-109">Inicializar Prepara um recurso para uso e o define como um estado padrão</span><span class="sxs-lookup"><span data-stu-id="0a2f3-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="0a2f3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0a2f3-110">PARAMETERS</span></span>

### <span data-ttu-id="0a2f3-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="0a2f3-111">-CodeDir</span></span>
<span data-ttu-id="0a2f3-112">O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="0a2f3-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="0a2f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2f3-113">-DefaultProfile</span></span>
<span data-ttu-id="0a2f3-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2f3-115">-Language</span><span class="sxs-lookup"><span data-stu-id="0a2f3-115">-Language</span></span>


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

### <span data-ttu-id="0a2f3-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="0a2f3-116">-ProjFileName</span></span>


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

### <span data-ttu-id="0a2f3-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a2f3-117">-SubscriptionId</span></span>
<span data-ttu-id="0a2f3-118">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2f3-118">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2f3-119">CommonParameters</span></span>
<span data-ttu-id="0a2f3-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a2f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2f3-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a2f3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2f3-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a2f3-122">INPUTS</span></span>

## <span data-ttu-id="0a2f3-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0a2f3-123">OUTPUTS</span></span>

### <span data-ttu-id="0a2f3-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="0a2f3-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="0a2f3-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="0a2f3-125">NOTES</span></span>

<span data-ttu-id="0a2f3-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0a2f3-126">ALIASES</span></span>

## <span data-ttu-id="0a2f3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a2f3-127">RELATED LINKS</span></span>

