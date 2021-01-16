---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257432"
---
# <span data-ttu-id="b9cda-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b9cda-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="b9cda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9cda-102">SYNOPSIS</span></span>
<span data-ttu-id="b9cda-103">Obtém os detalhes de um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="b9cda-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="b9cda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9cda-104">SYNTAX</span></span>

### <span data-ttu-id="b9cda-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9cda-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9cda-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b9cda-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9cda-107">List1</span><span class="sxs-lookup"><span data-stu-id="b9cda-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b9cda-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9cda-108">DESCRIPTION</span></span>
<span data-ttu-id="b9cda-109">Obtém os detalhes de um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="b9cda-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="b9cda-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9cda-110">EXAMPLES</span></span>

### <span data-ttu-id="b9cda-111">Exemplo 1: listar todos os contêineres de proteção no cofre e na malha</span><span class="sxs-lookup"><span data-stu-id="b9cda-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="b9cda-112">Lista todos.</span><span class="sxs-lookup"><span data-stu-id="b9cda-112">Lists all.</span></span>

### <span data-ttu-id="b9cda-113">Exemplo 2: obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="b9cda-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="b9cda-114">Obtém um específico.</span><span class="sxs-lookup"><span data-stu-id="b9cda-114">Gets a specific one.</span></span>

## <span data-ttu-id="b9cda-115">OS</span><span class="sxs-lookup"><span data-stu-id="b9cda-115">PARAMETERS</span></span>

### <span data-ttu-id="b9cda-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9cda-116">-DefaultProfile</span></span>
<span data-ttu-id="b9cda-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9cda-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9cda-118">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="b9cda-118">-FabricName</span></span>
<span data-ttu-id="b9cda-119">Nome do tecido.</span><span class="sxs-lookup"><span data-stu-id="b9cda-119">Fabric name.</span></span>

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

### <span data-ttu-id="b9cda-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="b9cda-120">-ProtectionContainerName</span></span>
<span data-ttu-id="b9cda-121">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="b9cda-121">Protection container name.</span></span>

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

### <span data-ttu-id="b9cda-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9cda-122">-ResourceGroupName</span></span>
<span data-ttu-id="b9cda-123">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="b9cda-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="b9cda-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b9cda-124">-ResourceName</span></span>
<span data-ttu-id="b9cda-125">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b9cda-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="b9cda-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9cda-126">-SubscriptionId</span></span>
<span data-ttu-id="b9cda-127">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9cda-127">The subscription Id.</span></span>

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

### <span data-ttu-id="b9cda-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9cda-128">CommonParameters</span></span>
<span data-ttu-id="b9cda-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9cda-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9cda-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9cda-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9cda-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9cda-131">INPUTS</span></span>

## <span data-ttu-id="b9cda-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9cda-132">OUTPUTS</span></span>

### <span data-ttu-id="b9cda-133">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b9cda-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="b9cda-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9cda-134">NOTES</span></span>

<span data-ttu-id="b9cda-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b9cda-135">ALIASES</span></span>

## <span data-ttu-id="b9cda-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9cda-136">RELATED LINKS</span></span>

