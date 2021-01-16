---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259850"
---
# <span data-ttu-id="689f1-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="689f1-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="689f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="689f1-102">SYNOPSIS</span></span>
<span data-ttu-id="689f1-103">Obtém os detalhes de uma política de replicação.</span><span class="sxs-lookup"><span data-stu-id="689f1-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="689f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="689f1-104">SYNTAX</span></span>

### <span data-ttu-id="689f1-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="689f1-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="689f1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="689f1-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="689f1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="689f1-107">DESCRIPTION</span></span>
<span data-ttu-id="689f1-108">Obtém os detalhes de uma política de replicação.</span><span class="sxs-lookup"><span data-stu-id="689f1-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="689f1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="689f1-109">EXAMPLES</span></span>

### <span data-ttu-id="689f1-110">Exemplo 1: obter todas as políticas em um cofre</span><span class="sxs-lookup"><span data-stu-id="689f1-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="689f1-111">Obter todas as políticas.</span><span class="sxs-lookup"><span data-stu-id="689f1-111">Get all policies.</span></span>

### <span data-ttu-id="689f1-112">Exemplo 2: obter uma política específica</span><span class="sxs-lookup"><span data-stu-id="689f1-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="689f1-113">Obter um específico.</span><span class="sxs-lookup"><span data-stu-id="689f1-113">Get a specific one.</span></span>

## <span data-ttu-id="689f1-114">OS</span><span class="sxs-lookup"><span data-stu-id="689f1-114">PARAMETERS</span></span>

### <span data-ttu-id="689f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689f1-115">-DefaultProfile</span></span>
<span data-ttu-id="689f1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="689f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="689f1-117">-Políticaname</span><span class="sxs-lookup"><span data-stu-id="689f1-117">-PolicyName</span></span>
<span data-ttu-id="689f1-118">Nome da política de replicação.</span><span class="sxs-lookup"><span data-stu-id="689f1-118">Replication policy name.</span></span>

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

### <span data-ttu-id="689f1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="689f1-119">-ResourceGroupName</span></span>
<span data-ttu-id="689f1-120">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="689f1-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="689f1-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="689f1-121">-ResourceName</span></span>
<span data-ttu-id="689f1-122">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="689f1-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="689f1-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="689f1-123">-SubscriptionId</span></span>
<span data-ttu-id="689f1-124">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="689f1-124">The subscription Id.</span></span>

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

### <span data-ttu-id="689f1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689f1-125">CommonParameters</span></span>
<span data-ttu-id="689f1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="689f1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689f1-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="689f1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689f1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="689f1-128">INPUTS</span></span>

## <span data-ttu-id="689f1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="689f1-129">OUTPUTS</span></span>

### <span data-ttu-id="689f1-130">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="689f1-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="689f1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="689f1-131">NOTES</span></span>

<span data-ttu-id="689f1-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="689f1-132">ALIASES</span></span>

## <span data-ttu-id="689f1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="689f1-133">RELATED LINKS</span></span>

