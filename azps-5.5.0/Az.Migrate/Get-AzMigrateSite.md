---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111769"
---
# <span data-ttu-id="0b730-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="0b730-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="0b730-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b730-102">SYNOPSIS</span></span>
<span data-ttu-id="0b730-103">Método para obter um site.</span><span class="sxs-lookup"><span data-stu-id="0b730-103">Method to get a site.</span></span>

## <span data-ttu-id="0b730-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b730-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0b730-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b730-105">DESCRIPTION</span></span>
<span data-ttu-id="0b730-106">Método para obter um site.</span><span class="sxs-lookup"><span data-stu-id="0b730-106">Method to get a site.</span></span>

## <span data-ttu-id="0b730-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b730-107">EXAMPLES</span></span>

### <span data-ttu-id="0b730-108">Exemplo 1: Obter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b730-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="0b730-109">Obter site por nome</span><span class="sxs-lookup"><span data-stu-id="0b730-109">Get site by name</span></span>

## <span data-ttu-id="0b730-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b730-110">PARAMETERS</span></span>

### <span data-ttu-id="0b730-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b730-111">-DefaultProfile</span></span>
<span data-ttu-id="0b730-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b730-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b730-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b730-113">-Name</span></span>
<span data-ttu-id="0b730-114">Nome do site.</span><span class="sxs-lookup"><span data-stu-id="0b730-114">Site name.</span></span>

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

### <span data-ttu-id="0b730-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b730-115">-ResourceGroupName</span></span>
<span data-ttu-id="0b730-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b730-116">The name of the resource group.</span></span>
<span data-ttu-id="0b730-117">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0b730-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0b730-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b730-118">-SubscriptionId</span></span>
<span data-ttu-id="0b730-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0b730-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0b730-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b730-120">CommonParameters</span></span>
<span data-ttu-id="0b730-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b730-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b730-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b730-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b730-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="0b730-123">INPUTS</span></span>

## <span data-ttu-id="0b730-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="0b730-124">OUTPUTS</span></span>

### <span data-ttu-id="0b730-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVSite</span><span class="sxs-lookup"><span data-stu-id="0b730-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="0b730-126">Notas</span><span class="sxs-lookup"><span data-stu-id="0b730-126">NOTES</span></span>

<span data-ttu-id="0b730-127">Aliases</span><span class="sxs-lookup"><span data-stu-id="0b730-127">ALIASES</span></span>

## <span data-ttu-id="0b730-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b730-128">RELATED LINKS</span></span>

