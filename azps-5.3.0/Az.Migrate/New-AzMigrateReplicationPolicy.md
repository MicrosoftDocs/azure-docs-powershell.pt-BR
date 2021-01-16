---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426747"
---
# <span data-ttu-id="9634b-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="9634b-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="9634b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9634b-102">SYNOPSIS</span></span>
<span data-ttu-id="9634b-103">A operação para criar uma política de replicação</span><span class="sxs-lookup"><span data-stu-id="9634b-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="9634b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9634b-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9634b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9634b-105">DESCRIPTION</span></span>
<span data-ttu-id="9634b-106">A operação para criar uma política de replicação</span><span class="sxs-lookup"><span data-stu-id="9634b-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="9634b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9634b-107">EXAMPLES</span></span>

### <span data-ttu-id="9634b-108">Exemplo 1: criar uma política de replicação</span><span class="sxs-lookup"><span data-stu-id="9634b-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="9634b-109">Cria uma política para o VmWare CBT</span><span class="sxs-lookup"><span data-stu-id="9634b-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="9634b-110">OS</span><span class="sxs-lookup"><span data-stu-id="9634b-110">PARAMETERS</span></span>

### <span data-ttu-id="9634b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9634b-111">-AsJob</span></span>
<span data-ttu-id="9634b-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9634b-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9634b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9634b-113">-DefaultProfile</span></span>
<span data-ttu-id="9634b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9634b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9634b-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9634b-115">-NoWait</span></span>
<span data-ttu-id="9634b-116">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="9634b-116">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9634b-117">-Políticaname</span><span class="sxs-lookup"><span data-stu-id="9634b-117">-PolicyName</span></span>
<span data-ttu-id="9634b-118">Nome da política de replicação</span><span class="sxs-lookup"><span data-stu-id="9634b-118">Replication policy name</span></span>

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

### <span data-ttu-id="9634b-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="9634b-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="9634b-120">O ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="9634b-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="9634b-121">Para construir, consulte a seção notas para propriedades PROVIDERSPECIFICINPUT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9634b-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9634b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9634b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9634b-123">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="9634b-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="9634b-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9634b-124">-ResourceName</span></span>
<span data-ttu-id="9634b-125">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="9634b-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="9634b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9634b-126">-SubscriptionId</span></span>
<span data-ttu-id="9634b-127">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9634b-127">The subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9634b-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9634b-128">-Confirm</span></span>
<span data-ttu-id="9634b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9634b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9634b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9634b-130">-WhatIf</span></span>
<span data-ttu-id="9634b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9634b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9634b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9634b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9634b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9634b-133">CommonParameters</span></span>
<span data-ttu-id="9634b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9634b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9634b-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9634b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9634b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9634b-136">INPUTS</span></span>

## <span data-ttu-id="9634b-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9634b-137">OUTPUTS</span></span>

### <span data-ttu-id="9634b-138">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="9634b-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="9634b-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9634b-139">NOTES</span></span>

<span data-ttu-id="9634b-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9634b-140">ALIASES</span></span>

<span data-ttu-id="9634b-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="9634b-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9634b-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9634b-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9634b-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9634b-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9634b-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="9634b-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="9634b-145">`[InstanceType <String>]`: O tipo de classe.</span><span class="sxs-lookup"><span data-stu-id="9634b-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="9634b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9634b-146">RELATED LINKS</span></span>

