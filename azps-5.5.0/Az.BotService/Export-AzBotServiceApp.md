---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116931"
---
# <span data-ttu-id="f2b73-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="f2b73-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="f2b73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2b73-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b73-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f2b73-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="f2b73-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2b73-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f2b73-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2b73-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b73-106">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f2b73-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="f2b73-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2b73-107">EXAMPLES</span></span>

### <span data-ttu-id="f2b73-108">Exemplo 1: Carregar a pasta Aplicativo BotService</span><span class="sxs-lookup"><span data-stu-id="f2b73-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="f2b73-109">Carregar a pasta Aplicativo BotService</span><span class="sxs-lookup"><span data-stu-id="f2b73-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="f2b73-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2b73-110">PARAMETERS</span></span>

### <span data-ttu-id="f2b73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b73-111">-DefaultProfile</span></span>
<span data-ttu-id="f2b73-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b73-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2b73-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2b73-113">-Name</span></span>
<span data-ttu-id="f2b73-114">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="f2b73-114">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="f2b73-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b73-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2b73-116">O nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2b73-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="f2b73-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="f2b73-117">-SavePath</span></span>


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

### <span data-ttu-id="f2b73-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2b73-118">-SubscriptionId</span></span>
<span data-ttu-id="f2b73-119">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b73-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f2b73-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b73-120">CommonParameters</span></span>
<span data-ttu-id="f2b73-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b73-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b73-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2b73-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b73-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="f2b73-123">INPUTS</span></span>

## <span data-ttu-id="f2b73-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="f2b73-124">OUTPUTS</span></span>

### <span data-ttu-id="f2b73-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="f2b73-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="f2b73-126">Notas</span><span class="sxs-lookup"><span data-stu-id="f2b73-126">NOTES</span></span>

<span data-ttu-id="f2b73-127">Aliases</span><span class="sxs-lookup"><span data-stu-id="f2b73-127">ALIASES</span></span>

## <span data-ttu-id="f2b73-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2b73-128">RELATED LINKS</span></span>

