---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124819"
---
# <span data-ttu-id="97b08-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="97b08-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="97b08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97b08-102">SYNOPSIS</span></span>
<span data-ttu-id="97b08-103">Método para obter a conta Executar como.</span><span class="sxs-lookup"><span data-stu-id="97b08-103">Method to get run as account.</span></span>

## <span data-ttu-id="97b08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97b08-104">SYNTAX</span></span>

### <span data-ttu-id="97b08-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="97b08-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97b08-106">Obter</span><span class="sxs-lookup"><span data-stu-id="97b08-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="97b08-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97b08-107">DESCRIPTION</span></span>
<span data-ttu-id="97b08-108">Método para obter a conta Executar como.</span><span class="sxs-lookup"><span data-stu-id="97b08-108">Method to get run as account.</span></span>

## <span data-ttu-id="97b08-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97b08-109">EXAMPLES</span></span>

### <span data-ttu-id="97b08-110">Exemplo 1: lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="97b08-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="97b08-111">Lista todas as contas Executar como em um site.</span><span class="sxs-lookup"><span data-stu-id="97b08-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="97b08-112">Exemplo 2: obter</span><span class="sxs-lookup"><span data-stu-id="97b08-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="97b08-113">Obter uma conta Executar como por nome.</span><span class="sxs-lookup"><span data-stu-id="97b08-113">Get Run as account by name.</span></span>

## <span data-ttu-id="97b08-114">OS</span><span class="sxs-lookup"><span data-stu-id="97b08-114">PARAMETERS</span></span>

### <span data-ttu-id="97b08-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="97b08-115">-AccountName</span></span>
<span data-ttu-id="97b08-116">Executar como nome do braço da conta.</span><span class="sxs-lookup"><span data-stu-id="97b08-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="97b08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b08-117">-DefaultProfile</span></span>
<span data-ttu-id="97b08-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97b08-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97b08-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b08-119">-ResourceGroupName</span></span>
<span data-ttu-id="97b08-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97b08-120">The name of the resource group.</span></span>
<span data-ttu-id="97b08-121">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="97b08-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="97b08-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="97b08-122">-SiteName</span></span>
<span data-ttu-id="97b08-123">Nome do site.</span><span class="sxs-lookup"><span data-stu-id="97b08-123">Site name.</span></span>

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

### <span data-ttu-id="97b08-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97b08-124">-SubscriptionId</span></span>
<span data-ttu-id="97b08-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="97b08-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="97b08-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b08-126">CommonParameters</span></span>
<span data-ttu-id="97b08-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b08-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b08-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97b08-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b08-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97b08-129">INPUTS</span></span>

## <span data-ttu-id="97b08-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97b08-130">OUTPUTS</span></span>

### <span data-ttu-id="97b08-131">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api202001. IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="97b08-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="97b08-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97b08-132">NOTES</span></span>

<span data-ttu-id="97b08-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="97b08-133">ALIASES</span></span>

## <span data-ttu-id="97b08-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97b08-134">RELATED LINKS</span></span>

