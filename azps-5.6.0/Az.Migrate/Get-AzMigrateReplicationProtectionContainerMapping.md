---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 87fa8d8653d0409eb4b322e0ce21dbc9c8cfa668
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889241"
---
# <span data-ttu-id="e8eff-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e8eff-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="e8eff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8eff-102">SYNOPSIS</span></span>
<span data-ttu-id="e8eff-103">Obtém os detalhes de um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="e8eff-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="e8eff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e8eff-104">SYNTAX</span></span>

### <span data-ttu-id="e8eff-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e8eff-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e8eff-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e8eff-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e8eff-107">Listar</span><span class="sxs-lookup"><span data-stu-id="e8eff-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8eff-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e8eff-108">DESCRIPTION</span></span>
<span data-ttu-id="e8eff-109">Obtém os detalhes de um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="e8eff-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="e8eff-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8eff-110">EXAMPLES</span></span>

### <span data-ttu-id="e8eff-111">Exemplo 1: Obter um mapeamento específico</span><span class="sxs-lookup"><span data-stu-id="e8eff-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="e8eff-112">Obter um detalhe de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="e8eff-112">Get a mapping detail.</span></span>

## <span data-ttu-id="e8eff-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e8eff-113">PARAMETERS</span></span>

### <span data-ttu-id="e8eff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8eff-114">-DefaultProfile</span></span>
<span data-ttu-id="e8eff-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8eff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8eff-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="e8eff-116">-FabricName</span></span>
<span data-ttu-id="e8eff-117">Nome do fabric.</span><span class="sxs-lookup"><span data-stu-id="e8eff-117">Fabric name.</span></span>

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

### <span data-ttu-id="e8eff-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="e8eff-118">-MappingName</span></span>
<span data-ttu-id="e8eff-119">Nome do mapeamento do Contêiner de Proteção.</span><span class="sxs-lookup"><span data-stu-id="e8eff-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="e8eff-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="e8eff-120">-ProtectionContainerName</span></span>
<span data-ttu-id="e8eff-121">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="e8eff-121">Protection container name.</span></span>

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

### <span data-ttu-id="e8eff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8eff-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8eff-123">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="e8eff-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="e8eff-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e8eff-124">-ResourceName</span></span>
<span data-ttu-id="e8eff-125">O nome do cofre dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e8eff-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="e8eff-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8eff-126">-SubscriptionId</span></span>
<span data-ttu-id="e8eff-127">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="e8eff-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="e8eff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8eff-128">CommonParameters</span></span>
<span data-ttu-id="e8eff-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8eff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8eff-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8eff-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8eff-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8eff-131">INPUTS</span></span>

## <span data-ttu-id="e8eff-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e8eff-132">OUTPUTS</span></span>

### <span data-ttu-id="e8eff-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e8eff-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="e8eff-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="e8eff-134">NOTES</span></span>

<span data-ttu-id="e8eff-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e8eff-135">ALIASES</span></span>

## <span data-ttu-id="e8eff-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8eff-136">RELATED LINKS</span></span>

