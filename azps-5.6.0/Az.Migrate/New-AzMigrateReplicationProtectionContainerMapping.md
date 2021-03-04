---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: ddbc4b9176405dd3102ba82cbe1954a876c9c7f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888933"
---
# <span data-ttu-id="6b9e7-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6b9e7-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="6b9e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9e7-103">A operação para criar um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="6b9e7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6b9e7-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6b9e7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6b9e7-105">DESCRIPTION</span></span>
<span data-ttu-id="6b9e7-106">A operação para criar um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="6b9e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b9e7-107">EXAMPLES</span></span>

### <span data-ttu-id="6b9e7-108">Exemplo 1: Criar um mapeamento</span><span class="sxs-lookup"><span data-stu-id="6b9e7-108">Example 1: Create a mapping</span></span>
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

<span data-ttu-id="6b9e7-109">Criar um mapeamento</span><span class="sxs-lookup"><span data-stu-id="6b9e7-109">Create a mapping</span></span>

## <span data-ttu-id="6b9e7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6b9e7-110">PARAMETERS</span></span>

### <span data-ttu-id="6b9e7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b9e7-111">-AsJob</span></span>
<span data-ttu-id="6b9e7-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6b9e7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6b9e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9e7-113">-DefaultProfile</span></span>
<span data-ttu-id="6b9e7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b9e7-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="6b9e7-115">-FabricName</span></span>
<span data-ttu-id="6b9e7-116">Nome do fabric.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-116">Fabric name.</span></span>

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

### <span data-ttu-id="6b9e7-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="6b9e7-117">-MappingName</span></span>
<span data-ttu-id="6b9e7-118">Nome do mapeamento do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="6b9e7-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6b9e7-119">-NoWait</span></span>
<span data-ttu-id="6b9e7-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6b9e7-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6b9e7-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="6b9e7-121">-PolicyId</span></span>
<span data-ttu-id="6b9e7-122">Política aplicável.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-122">Applicable policy.</span></span>

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

### <span data-ttu-id="6b9e7-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="6b9e7-123">-ProtectionContainerName</span></span>
<span data-ttu-id="6b9e7-124">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-124">Protection container name.</span></span>

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

### <span data-ttu-id="6b9e7-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="6b9e7-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="6b9e7-126">Entrada específica do provedor para emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="6b9e7-127">Para construir, consulte a seção NOTES para propriedades PROVIDERSPECIFICINPUT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b9e7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b9e7-128">-ResourceGroupName</span></span>
<span data-ttu-id="6b9e7-129">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="6b9e7-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b9e7-130">-ResourceName</span></span>
<span data-ttu-id="6b9e7-131">O nome do cofre dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="6b9e7-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b9e7-132">-SubscriptionId</span></span>
<span data-ttu-id="6b9e7-133">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-133">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="6b9e7-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="6b9e7-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="6b9e7-135">O nome do contêiner de proteção exclusivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="6b9e7-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b9e7-136">-Confirm</span></span>
<span data-ttu-id="6b9e7-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b9e7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b9e7-138">-WhatIf</span></span>
<span data-ttu-id="6b9e7-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b9e7-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b9e7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9e7-141">CommonParameters</span></span>
<span data-ttu-id="6b9e7-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9e7-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b9e7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9e7-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b9e7-144">INPUTS</span></span>

## <span data-ttu-id="6b9e7-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6b9e7-145">OUTPUTS</span></span>

### <span data-ttu-id="6b9e7-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6b9e7-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="6b9e7-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="6b9e7-147">NOTES</span></span>

<span data-ttu-id="6b9e7-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6b9e7-148">ALIASES</span></span>

<span data-ttu-id="6b9e7-149">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="6b9e7-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b9e7-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b9e7-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b9e7-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : Entrada específica do provedor para emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="6b9e7-153">`[InstanceType <String>]`: O tipo de classe.</span><span class="sxs-lookup"><span data-stu-id="6b9e7-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="6b9e7-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b9e7-154">RELATED LINKS</span></span>

