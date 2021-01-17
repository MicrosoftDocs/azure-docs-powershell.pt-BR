---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433543"
---
# <span data-ttu-id="ad067-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="ad067-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="ad067-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad067-102">SYNOPSIS</span></span>
<span data-ttu-id="ad067-103">Obtém os detalhes de uma política de replicação.</span><span class="sxs-lookup"><span data-stu-id="ad067-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="ad067-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad067-104">SYNTAX</span></span>

### <span data-ttu-id="ad067-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="ad067-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ad067-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ad067-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ad067-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad067-107">DESCRIPTION</span></span>
<span data-ttu-id="ad067-108">Obtém os detalhes de uma política de replicação.</span><span class="sxs-lookup"><span data-stu-id="ad067-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="ad067-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad067-109">EXAMPLES</span></span>

### <span data-ttu-id="ad067-110">Exemplo 1: obter todas as políticas em um cofre</span><span class="sxs-lookup"><span data-stu-id="ad067-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="ad067-111">Obter todas as políticas.</span><span class="sxs-lookup"><span data-stu-id="ad067-111">Get all policies.</span></span>

### <span data-ttu-id="ad067-112">Exemplo 2: obter uma política específica</span><span class="sxs-lookup"><span data-stu-id="ad067-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="ad067-113">Obter um específico.</span><span class="sxs-lookup"><span data-stu-id="ad067-113">Get a specific one.</span></span>

## <span data-ttu-id="ad067-114">OS</span><span class="sxs-lookup"><span data-stu-id="ad067-114">PARAMETERS</span></span>

### <span data-ttu-id="ad067-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad067-115">-DefaultProfile</span></span>
<span data-ttu-id="ad067-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad067-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad067-117">-Políticaname</span><span class="sxs-lookup"><span data-stu-id="ad067-117">-PolicyName</span></span>
<span data-ttu-id="ad067-118">Nome da política de replicação.</span><span class="sxs-lookup"><span data-stu-id="ad067-118">Replication policy name.</span></span>

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

### <span data-ttu-id="ad067-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad067-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad067-120">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="ad067-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="ad067-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ad067-121">-ResourceName</span></span>
<span data-ttu-id="ad067-122">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ad067-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="ad067-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad067-123">-SubscriptionId</span></span>
<span data-ttu-id="ad067-124">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ad067-124">The subscription Id.</span></span>

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

### <span data-ttu-id="ad067-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad067-125">CommonParameters</span></span>
<span data-ttu-id="ad067-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad067-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad067-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad067-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad067-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad067-128">INPUTS</span></span>

## <span data-ttu-id="ad067-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad067-129">OUTPUTS</span></span>

### <span data-ttu-id="ad067-130">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="ad067-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="ad067-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad067-131">NOTES</span></span>

<span data-ttu-id="ad067-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ad067-132">ALIASES</span></span>

## <span data-ttu-id="ad067-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad067-133">RELATED LINKS</span></span>

