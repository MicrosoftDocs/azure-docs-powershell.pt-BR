---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: 7a1cec73706d1ed799966bc3d97da06867139c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889243"
---
# <span data-ttu-id="67ff3-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="67ff3-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="67ff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="67ff3-103">Obtém os detalhes de um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="67ff3-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="67ff3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="67ff3-104">SYNTAX</span></span>

### <span data-ttu-id="67ff3-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="67ff3-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67ff3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="67ff3-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="67ff3-107">Listar</span><span class="sxs-lookup"><span data-stu-id="67ff3-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="67ff3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="67ff3-108">DESCRIPTION</span></span>
<span data-ttu-id="67ff3-109">Obtém os detalhes de um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="67ff3-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="67ff3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67ff3-110">EXAMPLES</span></span>

### <span data-ttu-id="67ff3-111">Exemplo 1: listar todos os contêineres de proteção em cofre e malha</span><span class="sxs-lookup"><span data-stu-id="67ff3-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="67ff3-112">Lista tudo.</span><span class="sxs-lookup"><span data-stu-id="67ff3-112">Lists all.</span></span>

### <span data-ttu-id="67ff3-113">Exemplo 2: Obter um contêiner específico</span><span class="sxs-lookup"><span data-stu-id="67ff3-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="67ff3-114">Obtém um específico.</span><span class="sxs-lookup"><span data-stu-id="67ff3-114">Gets a specific one.</span></span>

## <span data-ttu-id="67ff3-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="67ff3-115">PARAMETERS</span></span>

### <span data-ttu-id="67ff3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ff3-116">-DefaultProfile</span></span>
<span data-ttu-id="67ff3-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67ff3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ff3-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="67ff3-118">-FabricName</span></span>
<span data-ttu-id="67ff3-119">Nome do fabric.</span><span class="sxs-lookup"><span data-stu-id="67ff3-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ff3-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="67ff3-120">-ProtectionContainerName</span></span>
<span data-ttu-id="67ff3-121">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="67ff3-121">Protection container name.</span></span>

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

### <span data-ttu-id="67ff3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ff3-122">-ResourceGroupName</span></span>
<span data-ttu-id="67ff3-123">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="67ff3-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="67ff3-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="67ff3-124">-ResourceName</span></span>
<span data-ttu-id="67ff3-125">O nome do cofre dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="67ff3-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="67ff3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67ff3-126">-SubscriptionId</span></span>
<span data-ttu-id="67ff3-127">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="67ff3-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="67ff3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ff3-128">CommonParameters</span></span>
<span data-ttu-id="67ff3-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ff3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ff3-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67ff3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ff3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67ff3-131">INPUTS</span></span>

## <span data-ttu-id="67ff3-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="67ff3-132">OUTPUTS</span></span>

### <span data-ttu-id="67ff3-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="67ff3-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="67ff3-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="67ff3-134">NOTES</span></span>

<span data-ttu-id="67ff3-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="67ff3-135">ALIASES</span></span>

## <span data-ttu-id="67ff3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67ff3-136">RELATED LINKS</span></span>

