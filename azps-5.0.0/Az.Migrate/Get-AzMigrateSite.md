---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124816"
---
# <span data-ttu-id="a36a2-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="a36a2-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="a36a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a36a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a36a2-103">Método para obter um site.</span><span class="sxs-lookup"><span data-stu-id="a36a2-103">Method to get a site.</span></span>

## <span data-ttu-id="a36a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a36a2-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a36a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a36a2-105">DESCRIPTION</span></span>
<span data-ttu-id="a36a2-106">Método para obter um site.</span><span class="sxs-lookup"><span data-stu-id="a36a2-106">Method to get a site.</span></span>

## <span data-ttu-id="a36a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a36a2-107">EXAMPLES</span></span>

### <span data-ttu-id="a36a2-108">Exemplo 1: Get (padrão)</span><span class="sxs-lookup"><span data-stu-id="a36a2-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="a36a2-109">Obter site por nome</span><span class="sxs-lookup"><span data-stu-id="a36a2-109">Get site by name</span></span>

## <span data-ttu-id="a36a2-110">OS</span><span class="sxs-lookup"><span data-stu-id="a36a2-110">PARAMETERS</span></span>

### <span data-ttu-id="a36a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36a2-111">-DefaultProfile</span></span>
<span data-ttu-id="a36a2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a36a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a36a2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a36a2-113">-Name</span></span>
<span data-ttu-id="a36a2-114">Nome do site.</span><span class="sxs-lookup"><span data-stu-id="a36a2-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36a2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a36a2-115">-ResourceGroupName</span></span>
<span data-ttu-id="a36a2-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a36a2-116">The name of the resource group.</span></span>
<span data-ttu-id="a36a2-117">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a36a2-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a36a2-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a36a2-118">-SubscriptionId</span></span>
<span data-ttu-id="a36a2-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a36a2-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a36a2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36a2-120">CommonParameters</span></span>
<span data-ttu-id="a36a2-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a36a2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36a2-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a36a2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36a2-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a36a2-123">INPUTS</span></span>

## <span data-ttu-id="a36a2-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a36a2-124">OUTPUTS</span></span>

### <span data-ttu-id="a36a2-125">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api202001. IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="a36a2-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="a36a2-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a36a2-126">NOTES</span></span>

<span data-ttu-id="a36a2-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a36a2-127">ALIASES</span></span>

## <span data-ttu-id="a36a2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a36a2-128">RELATED LINKS</span></span>

