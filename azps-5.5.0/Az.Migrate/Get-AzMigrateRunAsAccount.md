---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112992"
---
# <span data-ttu-id="25b98-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="25b98-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="25b98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25b98-102">SYNOPSIS</span></span>
<span data-ttu-id="25b98-103">Método para ser executado como conta.</span><span class="sxs-lookup"><span data-stu-id="25b98-103">Method to get run as account.</span></span>

## <span data-ttu-id="25b98-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25b98-104">SYNTAX</span></span>

### <span data-ttu-id="25b98-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25b98-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="25b98-106">Obter</span><span class="sxs-lookup"><span data-stu-id="25b98-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="25b98-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="25b98-107">DESCRIPTION</span></span>
<span data-ttu-id="25b98-108">Método para ser executado como conta.</span><span class="sxs-lookup"><span data-stu-id="25b98-108">Method to get run as account.</span></span>

## <span data-ttu-id="25b98-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25b98-109">EXAMPLES</span></span>

### <span data-ttu-id="25b98-110">Exemplo 1: Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25b98-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="25b98-111">Listar todos executados como contas em um site.</span><span class="sxs-lookup"><span data-stu-id="25b98-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="25b98-112">Exemplo 2: Obter</span><span class="sxs-lookup"><span data-stu-id="25b98-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="25b98-113">Obter Executar como conta por nome.</span><span class="sxs-lookup"><span data-stu-id="25b98-113">Get Run as account by name.</span></span>

## <span data-ttu-id="25b98-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25b98-114">PARAMETERS</span></span>

### <span data-ttu-id="25b98-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="25b98-115">-AccountName</span></span>
<span data-ttu-id="25b98-116">Execute como nome ARM da conta.</span><span class="sxs-lookup"><span data-stu-id="25b98-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="25b98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b98-117">-DefaultProfile</span></span>
<span data-ttu-id="25b98-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25b98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25b98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b98-119">-ResourceGroupName</span></span>
<span data-ttu-id="25b98-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25b98-120">The name of the resource group.</span></span>
<span data-ttu-id="25b98-121">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="25b98-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="25b98-122">-Nomedo Site</span><span class="sxs-lookup"><span data-stu-id="25b98-122">-SiteName</span></span>
<span data-ttu-id="25b98-123">Nome do site.</span><span class="sxs-lookup"><span data-stu-id="25b98-123">Site name.</span></span>

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

### <span data-ttu-id="25b98-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25b98-124">-SubscriptionId</span></span>
<span data-ttu-id="25b98-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="25b98-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="25b98-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b98-126">CommonParameters</span></span>
<span data-ttu-id="25b98-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25b98-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b98-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25b98-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b98-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="25b98-129">INPUTS</span></span>

## <span data-ttu-id="25b98-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="25b98-130">OUTPUTS</span></span>

### <span data-ttu-id="25b98-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IV Ltd.</span><span class="sxs-lookup"><span data-stu-id="25b98-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="25b98-132">Notas</span><span class="sxs-lookup"><span data-stu-id="25b98-132">NOTES</span></span>

<span data-ttu-id="25b98-133">Aliases</span><span class="sxs-lookup"><span data-stu-id="25b98-133">ALIASES</span></span>

## <span data-ttu-id="25b98-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25b98-134">RELATED LINKS</span></span>

