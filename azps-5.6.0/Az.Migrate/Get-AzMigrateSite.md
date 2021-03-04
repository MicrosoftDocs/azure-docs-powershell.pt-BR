---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: b00010096b39cd714f01f33012309f8528a5ae3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889236"
---
# <span data-ttu-id="26941-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="26941-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="26941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26941-102">SYNOPSIS</span></span>
<span data-ttu-id="26941-103">Método para obter um site.</span><span class="sxs-lookup"><span data-stu-id="26941-103">Method to get a site.</span></span>

## <span data-ttu-id="26941-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="26941-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="26941-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="26941-105">DESCRIPTION</span></span>
<span data-ttu-id="26941-106">Método para obter um site.</span><span class="sxs-lookup"><span data-stu-id="26941-106">Method to get a site.</span></span>

## <span data-ttu-id="26941-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26941-107">EXAMPLES</span></span>

### <span data-ttu-id="26941-108">Exemplo 1: Obter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="26941-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="26941-109">Obter site por nome</span><span class="sxs-lookup"><span data-stu-id="26941-109">Get site by name</span></span>

## <span data-ttu-id="26941-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="26941-110">PARAMETERS</span></span>

### <span data-ttu-id="26941-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26941-111">-DefaultProfile</span></span>
<span data-ttu-id="26941-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26941-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26941-113">-Name</span><span class="sxs-lookup"><span data-stu-id="26941-113">-Name</span></span>
<span data-ttu-id="26941-114">Nome do site.</span><span class="sxs-lookup"><span data-stu-id="26941-114">Site name.</span></span>

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

### <span data-ttu-id="26941-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26941-115">-ResourceGroupName</span></span>
<span data-ttu-id="26941-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="26941-116">The name of the resource group.</span></span>
<span data-ttu-id="26941-117">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="26941-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="26941-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26941-118">-SubscriptionId</span></span>
<span data-ttu-id="26941-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="26941-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="26941-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26941-120">CommonParameters</span></span>
<span data-ttu-id="26941-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26941-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26941-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26941-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26941-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26941-123">INPUTS</span></span>

## <span data-ttu-id="26941-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="26941-124">OUTPUTS</span></span>

### <span data-ttu-id="26941-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="26941-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="26941-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="26941-126">NOTES</span></span>

<span data-ttu-id="26941-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="26941-127">ALIASES</span></span>

## <span data-ttu-id="26941-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26941-128">RELATED LINKS</span></span>

