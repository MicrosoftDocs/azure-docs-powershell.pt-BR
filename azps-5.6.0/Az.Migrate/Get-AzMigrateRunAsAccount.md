---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: d028e66fc5f1f4b2c3ab520bd76615e8e9e79099
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889238"
---
# <span data-ttu-id="baa7c-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="baa7c-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="baa7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baa7c-102">SYNOPSIS</span></span>
<span data-ttu-id="baa7c-103">Método para ser executado como conta.</span><span class="sxs-lookup"><span data-stu-id="baa7c-103">Method to get run as account.</span></span>

## <span data-ttu-id="baa7c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="baa7c-104">SYNTAX</span></span>

### <span data-ttu-id="baa7c-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="baa7c-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="baa7c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="baa7c-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="baa7c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="baa7c-107">DESCRIPTION</span></span>
<span data-ttu-id="baa7c-108">Método para ser executado como conta.</span><span class="sxs-lookup"><span data-stu-id="baa7c-108">Method to get run as account.</span></span>

## <span data-ttu-id="baa7c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="baa7c-109">EXAMPLES</span></span>

### <span data-ttu-id="baa7c-110">Exemplo 1: Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="baa7c-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="baa7c-111">Listar todos executados como contas em um site.</span><span class="sxs-lookup"><span data-stu-id="baa7c-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="baa7c-112">Exemplo 2: Obter</span><span class="sxs-lookup"><span data-stu-id="baa7c-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="baa7c-113">Get Run as account by name.</span><span class="sxs-lookup"><span data-stu-id="baa7c-113">Get Run as account by name.</span></span>

## <span data-ttu-id="baa7c-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="baa7c-114">PARAMETERS</span></span>

### <span data-ttu-id="baa7c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="baa7c-115">-AccountName</span></span>
<span data-ttu-id="baa7c-116">Execute como nome ARM conta.</span><span class="sxs-lookup"><span data-stu-id="baa7c-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa7c-117">-DefaultProfile</span></span>
<span data-ttu-id="baa7c-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="baa7c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baa7c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa7c-119">-ResourceGroupName</span></span>
<span data-ttu-id="baa7c-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="baa7c-120">The name of the resource group.</span></span>
<span data-ttu-id="baa7c-121">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="baa7c-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="baa7c-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="baa7c-122">-SiteName</span></span>
<span data-ttu-id="baa7c-123">Nome do site.</span><span class="sxs-lookup"><span data-stu-id="baa7c-123">Site name.</span></span>

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

### <span data-ttu-id="baa7c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="baa7c-124">-SubscriptionId</span></span>
<span data-ttu-id="baa7c-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="baa7c-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="baa7c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa7c-126">CommonParameters</span></span>
<span data-ttu-id="baa7c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baa7c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa7c-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baa7c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa7c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baa7c-129">INPUTS</span></span>

## <span data-ttu-id="baa7c-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="baa7c-130">OUTPUTS</span></span>

### <span data-ttu-id="baa7c-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="baa7c-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="baa7c-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="baa7c-132">NOTES</span></span>

<span data-ttu-id="baa7c-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="baa7c-133">ALIASES</span></span>

## <span data-ttu-id="baa7c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baa7c-134">RELATED LINKS</span></span>

