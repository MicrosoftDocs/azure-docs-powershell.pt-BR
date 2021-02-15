---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5ea43fe8d79181cfe0215fc09949655fe430f532
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114253"
---
# <span data-ttu-id="b162f-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b162f-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="b162f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b162f-102">SYNOPSIS</span></span>
<span data-ttu-id="b162f-103">A operação para criar uma política de replicação</span><span class="sxs-lookup"><span data-stu-id="b162f-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="b162f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b162f-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b162f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b162f-105">DESCRIPTION</span></span>
<span data-ttu-id="b162f-106">A operação para criar uma política de replicação</span><span class="sxs-lookup"><span data-stu-id="b162f-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="b162f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b162f-107">EXAMPLES</span></span>

### <span data-ttu-id="b162f-108">Exemplo 1: Criar uma política de replicação</span><span class="sxs-lookup"><span data-stu-id="b162f-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="b162f-109">Cria uma política para o VmWare Cbt</span><span class="sxs-lookup"><span data-stu-id="b162f-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="b162f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b162f-110">PARAMETERS</span></span>

### <span data-ttu-id="b162f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b162f-111">-AsJob</span></span>
<span data-ttu-id="b162f-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b162f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b162f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b162f-113">-DefaultProfile</span></span>
<span data-ttu-id="b162f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b162f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b162f-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b162f-115">-NoWait</span></span>
<span data-ttu-id="b162f-116">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="b162f-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b162f-117">-Nomeda Política</span><span class="sxs-lookup"><span data-stu-id="b162f-117">-PolicyName</span></span>
<span data-ttu-id="b162f-118">Nome da política de replicação</span><span class="sxs-lookup"><span data-stu-id="b162f-118">Replication policy name</span></span>

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

### <span data-ttu-id="b162f-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="b162f-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="b162f-120">As ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="b162f-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="b162f-121">Para construir, confira a seção ANOTAÇÕES das propriedades PROVIDERSPECIFICINPUT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="b162f-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b162f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b162f-122">-ResourceGroupName</span></span>
<span data-ttu-id="b162f-123">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="b162f-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="b162f-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b162f-124">-ResourceName</span></span>
<span data-ttu-id="b162f-125">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b162f-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="b162f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b162f-126">-SubscriptionId</span></span>
<span data-ttu-id="b162f-127">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="b162f-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="b162f-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b162f-128">-Confirm</span></span>
<span data-ttu-id="b162f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b162f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b162f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b162f-130">-WhatIf</span></span>
<span data-ttu-id="b162f-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b162f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b162f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b162f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b162f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b162f-133">CommonParameters</span></span>
<span data-ttu-id="b162f-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b162f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b162f-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b162f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b162f-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="b162f-136">INPUTS</span></span>

## <span data-ttu-id="b162f-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="b162f-137">OUTPUTS</span></span>

### <span data-ttu-id="b162f-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="b162f-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="b162f-139">Notas</span><span class="sxs-lookup"><span data-stu-id="b162f-139">NOTES</span></span>

<span data-ttu-id="b162f-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="b162f-140">ALIASES</span></span>

<span data-ttu-id="b162f-141">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="b162f-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b162f-142">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b162f-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b162f-143">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b162f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b162f-144">PROVIDERSPECIFICINPUT: <IPolicyProviderSpecificInput> The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="b162f-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="b162f-145">`[InstanceType <String>]`: o tipo de classe.</span><span class="sxs-lookup"><span data-stu-id="b162f-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="b162f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b162f-146">RELATED LINKS</span></span>

