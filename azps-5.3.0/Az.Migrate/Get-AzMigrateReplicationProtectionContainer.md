---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427134"
---
# <span data-ttu-id="c9730-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c9730-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="c9730-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9730-102">SYNOPSIS</span></span>
<span data-ttu-id="c9730-103">Obtém os detalhes de um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="c9730-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="c9730-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9730-104">SYNTAX</span></span>

### <span data-ttu-id="c9730-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="c9730-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9730-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c9730-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9730-107">List1</span><span class="sxs-lookup"><span data-stu-id="c9730-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9730-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9730-108">DESCRIPTION</span></span>
<span data-ttu-id="c9730-109">Obtém os detalhes de um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="c9730-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="c9730-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9730-110">EXAMPLES</span></span>

### <span data-ttu-id="c9730-111">Exemplo 1: listar todos os contêineres de proteção no cofre e na malha</span><span class="sxs-lookup"><span data-stu-id="c9730-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="c9730-112">Lista todos.</span><span class="sxs-lookup"><span data-stu-id="c9730-112">Lists all.</span></span>

### <span data-ttu-id="c9730-113">Exemplo 2: obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="c9730-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="c9730-114">Obtém um específico.</span><span class="sxs-lookup"><span data-stu-id="c9730-114">Gets a specific one.</span></span>

## <span data-ttu-id="c9730-115">OS</span><span class="sxs-lookup"><span data-stu-id="c9730-115">PARAMETERS</span></span>

### <span data-ttu-id="c9730-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9730-116">-DefaultProfile</span></span>
<span data-ttu-id="c9730-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9730-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9730-118">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="c9730-118">-FabricName</span></span>
<span data-ttu-id="c9730-119">Nome do tecido.</span><span class="sxs-lookup"><span data-stu-id="c9730-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9730-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="c9730-120">-ProtectionContainerName</span></span>
<span data-ttu-id="c9730-121">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="c9730-121">Protection container name.</span></span>

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

### <span data-ttu-id="c9730-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9730-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9730-123">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="c9730-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="c9730-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c9730-124">-ResourceName</span></span>
<span data-ttu-id="c9730-125">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c9730-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="c9730-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9730-126">-SubscriptionId</span></span>
<span data-ttu-id="c9730-127">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="c9730-127">The subscription Id.</span></span>

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

### <span data-ttu-id="c9730-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9730-128">CommonParameters</span></span>
<span data-ttu-id="c9730-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9730-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9730-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9730-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9730-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9730-131">INPUTS</span></span>

## <span data-ttu-id="c9730-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9730-132">OUTPUTS</span></span>

### <span data-ttu-id="c9730-133">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c9730-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="c9730-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9730-134">NOTES</span></span>

<span data-ttu-id="c9730-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c9730-135">ALIASES</span></span>

## <span data-ttu-id="c9730-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9730-136">RELATED LINKS</span></span>

