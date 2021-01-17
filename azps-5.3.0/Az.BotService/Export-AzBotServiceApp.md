---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434460"
---
# <span data-ttu-id="c2d32-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="c2d32-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="c2d32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2d32-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d32-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c2d32-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="c2d32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2d32-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c2d32-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2d32-105">DESCRIPTION</span></span>
<span data-ttu-id="c2d32-106">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c2d32-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="c2d32-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2d32-107">EXAMPLES</span></span>

### <span data-ttu-id="c2d32-108">Exemplo 1: baixar a pasta de aplicativos BotService</span><span class="sxs-lookup"><span data-stu-id="c2d32-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="c2d32-109">Baixar a pasta de aplicativos BotService</span><span class="sxs-lookup"><span data-stu-id="c2d32-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="c2d32-110">OS</span><span class="sxs-lookup"><span data-stu-id="c2d32-110">PARAMETERS</span></span>

### <span data-ttu-id="c2d32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d32-111">-DefaultProfile</span></span>
<span data-ttu-id="c2d32-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d32-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2d32-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2d32-113">-Name</span></span>
<span data-ttu-id="c2d32-114">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="c2d32-114">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="c2d32-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d32-115">-ResourceGroupName</span></span>
<span data-ttu-id="c2d32-116">O nome do grupo de recursos de bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="c2d32-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="c2d32-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="c2d32-117">-SavePath</span></span>


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

### <span data-ttu-id="c2d32-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2d32-118">-SubscriptionId</span></span>
<span data-ttu-id="c2d32-119">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d32-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c2d32-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d32-120">CommonParameters</span></span>
<span data-ttu-id="c2d32-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2d32-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d32-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2d32-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d32-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2d32-123">INPUTS</span></span>

## <span data-ttu-id="c2d32-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2d32-124">OUTPUTS</span></span>

### <span data-ttu-id="c2d32-125">Microsoft. Azure. PowerShell. cmdlets. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="c2d32-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="c2d32-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2d32-126">NOTES</span></span>

<span data-ttu-id="c2d32-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c2d32-127">ALIASES</span></span>

## <span data-ttu-id="c2d32-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2d32-128">RELATED LINKS</span></span>

