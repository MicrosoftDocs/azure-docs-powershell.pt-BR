---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 996f33a967aaedc66bc0ed9b41cba09401f1dde4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115244"
---
# <span data-ttu-id="7eaf4-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7eaf4-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="7eaf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7eaf4-102">SYNOPSIS</span></span>
<span data-ttu-id="7eaf4-103">A operação para criar um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="7eaf4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7eaf4-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7eaf4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7eaf4-105">DESCRIPTION</span></span>
<span data-ttu-id="7eaf4-106">A operação para criar um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="7eaf4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7eaf4-107">EXAMPLES</span></span>

### <span data-ttu-id="7eaf4-108">Exemplo 1: Criar um mapeamento</span><span class="sxs-lookup"><span data-stu-id="7eaf4-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="7eaf4-109">Criar um mapeamento</span><span class="sxs-lookup"><span data-stu-id="7eaf4-109">Create a mapping</span></span>

## <span data-ttu-id="7eaf4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7eaf4-110">PARAMETERS</span></span>

### <span data-ttu-id="7eaf4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7eaf4-111">-AsJob</span></span>
<span data-ttu-id="7eaf4-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7eaf4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7eaf4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eaf4-113">-DefaultProfile</span></span>
<span data-ttu-id="7eaf4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eaf4-115">-NomeDaArmásia</span><span class="sxs-lookup"><span data-stu-id="7eaf4-115">-FabricName</span></span>
<span data-ttu-id="7eaf4-116">Nome do malha.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-116">Fabric name.</span></span>

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

### <span data-ttu-id="7eaf4-117">-NomeDo Mapeamento</span><span class="sxs-lookup"><span data-stu-id="7eaf4-117">-MappingName</span></span>
<span data-ttu-id="7eaf4-118">Nome de mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="7eaf4-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7eaf4-119">-NoWait</span></span>
<span data-ttu-id="7eaf4-120">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="7eaf4-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7eaf4-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="7eaf4-121">-PolicyId</span></span>
<span data-ttu-id="7eaf4-122">Política aplicável.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-122">Applicable policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf4-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="7eaf4-123">-ProtectionContainerName</span></span>
<span data-ttu-id="7eaf4-124">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-124">Protection container name.</span></span>

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

### <span data-ttu-id="7eaf4-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="7eaf4-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="7eaf4-126">Entrada específica do provedor para emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="7eaf4-127">Para construir, confira a seção ANOTAÇÕES das propriedades PROVIDERSPECIFICINPUT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eaf4-128">-ResourceGroupName</span></span>
<span data-ttu-id="7eaf4-129">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="7eaf4-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7eaf4-130">-ResourceName</span></span>
<span data-ttu-id="7eaf4-131">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="7eaf4-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7eaf4-132">-SubscriptionId</span></span>
<span data-ttu-id="7eaf4-133">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-133">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="7eaf4-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="7eaf4-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="7eaf4-135">O nome do contêiner de proteção exclusivo de destino.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-135">The target unique protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf4-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7eaf4-136">-Confirm</span></span>
<span data-ttu-id="7eaf4-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eaf4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eaf4-138">-WhatIf</span></span>
<span data-ttu-id="7eaf4-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eaf4-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eaf4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eaf4-141">CommonParameters</span></span>
<span data-ttu-id="7eaf4-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eaf4-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7eaf4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eaf4-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="7eaf4-144">INPUTS</span></span>

## <span data-ttu-id="7eaf4-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="7eaf4-145">OUTPUTS</span></span>

### <span data-ttu-id="7eaf4-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7eaf4-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="7eaf4-147">Notas</span><span class="sxs-lookup"><span data-stu-id="7eaf4-147">NOTES</span></span>

<span data-ttu-id="7eaf4-148">Aliases</span><span class="sxs-lookup"><span data-stu-id="7eaf4-148">ALIASES</span></span>

<span data-ttu-id="7eaf4-149">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="7eaf4-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7eaf4-150">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7eaf4-151">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7eaf4-152">PROVIDERSPECIFICINPUT: <IReplicationProviderSpecificContainerMappingInput> Entrada específica do provedor para emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="7eaf4-153">`[InstanceType <String>]`: o tipo de classe.</span><span class="sxs-lookup"><span data-stu-id="7eaf4-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="7eaf4-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7eaf4-154">RELATED LINKS</span></span>

