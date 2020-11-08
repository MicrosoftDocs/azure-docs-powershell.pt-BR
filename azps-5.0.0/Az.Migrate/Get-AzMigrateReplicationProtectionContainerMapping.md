---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126006"
---
# <span data-ttu-id="486be-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="486be-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="486be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="486be-102">SYNOPSIS</span></span>
<span data-ttu-id="486be-103">Obtém os detalhes de um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="486be-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="486be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="486be-104">SYNTAX</span></span>

### <span data-ttu-id="486be-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="486be-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="486be-106">Obter</span><span class="sxs-lookup"><span data-stu-id="486be-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="486be-107">Programação</span><span class="sxs-lookup"><span data-stu-id="486be-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="486be-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="486be-108">DESCRIPTION</span></span>
<span data-ttu-id="486be-109">Obtém os detalhes de um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="486be-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="486be-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="486be-110">EXAMPLES</span></span>

### <span data-ttu-id="486be-111">Exemplo 1: obter um mapeamento específico</span><span class="sxs-lookup"><span data-stu-id="486be-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="486be-112">Obter um detalhe de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="486be-112">Get a mapping detail.</span></span>

## <span data-ttu-id="486be-113">OS</span><span class="sxs-lookup"><span data-stu-id="486be-113">PARAMETERS</span></span>

### <span data-ttu-id="486be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486be-114">-DefaultProfile</span></span>
<span data-ttu-id="486be-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="486be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="486be-116">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="486be-116">-FabricName</span></span>
<span data-ttu-id="486be-117">Nome do tecido.</span><span class="sxs-lookup"><span data-stu-id="486be-117">Fabric name.</span></span>

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

### <span data-ttu-id="486be-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="486be-118">-MappingName</span></span>
<span data-ttu-id="486be-119">Nome do mapeamento do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="486be-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="486be-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="486be-120">-ProtectionContainerName</span></span>
<span data-ttu-id="486be-121">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="486be-121">Protection container name.</span></span>

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

### <span data-ttu-id="486be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="486be-122">-ResourceGroupName</span></span>
<span data-ttu-id="486be-123">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="486be-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="486be-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="486be-124">-ResourceName</span></span>
<span data-ttu-id="486be-125">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="486be-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="486be-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="486be-126">-SubscriptionId</span></span>
<span data-ttu-id="486be-127">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="486be-127">The subscription Id.</span></span>

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

### <span data-ttu-id="486be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486be-128">CommonParameters</span></span>
<span data-ttu-id="486be-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="486be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486be-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="486be-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486be-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="486be-131">INPUTS</span></span>

## <span data-ttu-id="486be-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="486be-132">OUTPUTS</span></span>

### <span data-ttu-id="486be-133">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="486be-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="486be-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="486be-134">NOTES</span></span>

<span data-ttu-id="486be-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="486be-135">ALIASES</span></span>

## <span data-ttu-id="486be-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="486be-136">RELATED LINKS</span></span>

