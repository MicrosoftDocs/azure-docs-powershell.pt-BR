---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: e2cad9282e1e662cee58625a17c3f0672947d26a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114260"
---
# <span data-ttu-id="d6481-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="d6481-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="d6481-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6481-102">SYNOPSIS</span></span>
<span data-ttu-id="d6481-103">Obtém os detalhes de uma política de replicação.</span><span class="sxs-lookup"><span data-stu-id="d6481-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="d6481-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6481-104">SYNTAX</span></span>

### <span data-ttu-id="d6481-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d6481-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6481-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d6481-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d6481-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6481-107">DESCRIPTION</span></span>
<span data-ttu-id="d6481-108">Obtém os detalhes de uma política de replicação.</span><span class="sxs-lookup"><span data-stu-id="d6481-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="d6481-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6481-109">EXAMPLES</span></span>

### <span data-ttu-id="d6481-110">Exemplo 1: Obter todas as políticas em um cofre</span><span class="sxs-lookup"><span data-stu-id="d6481-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="d6481-111">Obter todas as políticas.</span><span class="sxs-lookup"><span data-stu-id="d6481-111">Get all policies.</span></span>

### <span data-ttu-id="d6481-112">Exemplo 2: Obter uma política específica</span><span class="sxs-lookup"><span data-stu-id="d6481-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="d6481-113">Obter uma específica.</span><span class="sxs-lookup"><span data-stu-id="d6481-113">Get a specific one.</span></span>

## <span data-ttu-id="d6481-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6481-114">PARAMETERS</span></span>

### <span data-ttu-id="d6481-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6481-115">-DefaultProfile</span></span>
<span data-ttu-id="d6481-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6481-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6481-117">-Nomeda Política</span><span class="sxs-lookup"><span data-stu-id="d6481-117">-PolicyName</span></span>
<span data-ttu-id="d6481-118">Nome da política de replicação.</span><span class="sxs-lookup"><span data-stu-id="d6481-118">Replication policy name.</span></span>

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

### <span data-ttu-id="d6481-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6481-119">-ResourceGroupName</span></span>
<span data-ttu-id="d6481-120">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="d6481-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="d6481-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d6481-121">-ResourceName</span></span>
<span data-ttu-id="d6481-122">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d6481-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="d6481-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6481-123">-SubscriptionId</span></span>
<span data-ttu-id="d6481-124">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="d6481-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d6481-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6481-125">CommonParameters</span></span>
<span data-ttu-id="d6481-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6481-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6481-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6481-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6481-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="d6481-128">INPUTS</span></span>

## <span data-ttu-id="d6481-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="d6481-129">OUTPUTS</span></span>

### <span data-ttu-id="d6481-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="d6481-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="d6481-131">Notas</span><span class="sxs-lookup"><span data-stu-id="d6481-131">NOTES</span></span>

<span data-ttu-id="d6481-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="d6481-132">ALIASES</span></span>

## <span data-ttu-id="d6481-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6481-133">RELATED LINKS</span></span>

