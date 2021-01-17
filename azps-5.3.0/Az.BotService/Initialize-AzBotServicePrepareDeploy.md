---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434459"
---
# <span data-ttu-id="b35d8-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="b35d8-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="b35d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b35d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b35d8-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b35d8-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="b35d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b35d8-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b35d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b35d8-105">DESCRIPTION</span></span>
<span data-ttu-id="b35d8-106">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b35d8-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="b35d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b35d8-107">EXAMPLES</span></span>

### <span data-ttu-id="b35d8-108">Exemplo 1: inicializar a pasta de arquivo do projeto</span><span class="sxs-lookup"><span data-stu-id="b35d8-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="b35d8-109">Initialize prepara um recurso para uso e define-o como um estado padrão</span><span class="sxs-lookup"><span data-stu-id="b35d8-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="b35d8-110">OS</span><span class="sxs-lookup"><span data-stu-id="b35d8-110">PARAMETERS</span></span>

### <span data-ttu-id="b35d8-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="b35d8-111">-CodeDir</span></span>
<span data-ttu-id="b35d8-112">O nome do grupo de recursos de bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="b35d8-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="b35d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35d8-113">-DefaultProfile</span></span>
<span data-ttu-id="b35d8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b35d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b35d8-115">-Idioma</span><span class="sxs-lookup"><span data-stu-id="b35d8-115">-Language</span></span>


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

### <span data-ttu-id="b35d8-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="b35d8-116">-ProjFileName</span></span>


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

### <span data-ttu-id="b35d8-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b35d8-117">-SubscriptionId</span></span>
<span data-ttu-id="b35d8-118">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b35d8-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b35d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35d8-119">CommonParameters</span></span>
<span data-ttu-id="b35d8-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35d8-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b35d8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35d8-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b35d8-122">INPUTS</span></span>

## <span data-ttu-id="b35d8-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b35d8-123">OUTPUTS</span></span>

### <span data-ttu-id="b35d8-124">Microsoft. Azure. PowerShell. cmdlets. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="b35d8-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="b35d8-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b35d8-125">NOTES</span></span>

<span data-ttu-id="b35d8-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b35d8-126">ALIASES</span></span>

## <span data-ttu-id="b35d8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b35d8-127">RELATED LINKS</span></span>

