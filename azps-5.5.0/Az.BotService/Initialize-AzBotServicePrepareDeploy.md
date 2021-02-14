---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116930"
---
# <span data-ttu-id="40a81-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="40a81-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="40a81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40a81-102">SYNOPSIS</span></span>
<span data-ttu-id="40a81-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="40a81-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="40a81-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40a81-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="40a81-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="40a81-105">DESCRIPTION</span></span>
<span data-ttu-id="40a81-106">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="40a81-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="40a81-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40a81-107">EXAMPLES</span></span>

### <span data-ttu-id="40a81-108">Exemplo 1: Inicializar a Pasta de Arquivos do Project</span><span class="sxs-lookup"><span data-stu-id="40a81-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="40a81-109">Inicializar prepara um recurso para uso e o define como um estado padrão</span><span class="sxs-lookup"><span data-stu-id="40a81-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="40a81-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40a81-110">PARAMETERS</span></span>

### <span data-ttu-id="40a81-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="40a81-111">-CodeDir</span></span>
<span data-ttu-id="40a81-112">O nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="40a81-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="40a81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a81-113">-DefaultProfile</span></span>
<span data-ttu-id="40a81-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40a81-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40a81-115">-Idioma</span><span class="sxs-lookup"><span data-stu-id="40a81-115">-Language</span></span>


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

### <span data-ttu-id="40a81-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="40a81-116">-ProjFileName</span></span>


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

### <span data-ttu-id="40a81-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40a81-117">-SubscriptionId</span></span>
<span data-ttu-id="40a81-118">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="40a81-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="40a81-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a81-119">CommonParameters</span></span>
<span data-ttu-id="40a81-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40a81-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a81-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40a81-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a81-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="40a81-122">INPUTS</span></span>

## <span data-ttu-id="40a81-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="40a81-123">OUTPUTS</span></span>

### <span data-ttu-id="40a81-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="40a81-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="40a81-125">Notas</span><span class="sxs-lookup"><span data-stu-id="40a81-125">NOTES</span></span>

<span data-ttu-id="40a81-126">Aliases</span><span class="sxs-lookup"><span data-stu-id="40a81-126">ALIASES</span></span>

## <span data-ttu-id="40a81-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40a81-127">RELATED LINKS</span></span>

