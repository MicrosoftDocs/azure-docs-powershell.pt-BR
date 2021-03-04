---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: 79ef8a92997790f547847e05eae6ca101016bc42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886495"
---
# <span data-ttu-id="31420-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="31420-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="31420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31420-102">SYNOPSIS</span></span>
<span data-ttu-id="31420-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="31420-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="31420-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="31420-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="31420-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="31420-105">DESCRIPTION</span></span>
<span data-ttu-id="31420-106">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="31420-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="31420-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31420-107">EXAMPLES</span></span>

### <span data-ttu-id="31420-108">Exemplo 1: DownLoad da pasta Aplicativo BotService</span><span class="sxs-lookup"><span data-stu-id="31420-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="31420-109">DownLoad da pasta Aplicativo BotService</span><span class="sxs-lookup"><span data-stu-id="31420-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="31420-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="31420-110">PARAMETERS</span></span>

### <span data-ttu-id="31420-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31420-111">-DefaultProfile</span></span>
<span data-ttu-id="31420-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31420-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31420-113">-Name</span><span class="sxs-lookup"><span data-stu-id="31420-113">-Name</span></span>
<span data-ttu-id="31420-114">O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="31420-114">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31420-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31420-115">-ResourceGroupName</span></span>
<span data-ttu-id="31420-116">O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="31420-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="31420-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="31420-117">-SavePath</span></span>


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

### <span data-ttu-id="31420-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31420-118">-SubscriptionId</span></span>
<span data-ttu-id="31420-119">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="31420-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="31420-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31420-120">CommonParameters</span></span>
<span data-ttu-id="31420-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31420-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31420-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31420-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31420-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31420-123">INPUTS</span></span>

## <span data-ttu-id="31420-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="31420-124">OUTPUTS</span></span>

### <span data-ttu-id="31420-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="31420-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="31420-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="31420-126">NOTES</span></span>

<span data-ttu-id="31420-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="31420-127">ALIASES</span></span>

## <span data-ttu-id="31420-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31420-128">RELATED LINKS</span></span>

