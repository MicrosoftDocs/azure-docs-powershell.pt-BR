---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262165"
---
# <span data-ttu-id="3492b-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3492b-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="3492b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3492b-102">SYNOPSIS</span></span>
<span data-ttu-id="3492b-103">A operação para criar um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="3492b-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="3492b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3492b-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3492b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3492b-105">DESCRIPTION</span></span>
<span data-ttu-id="3492b-106">A operação para criar um mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="3492b-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="3492b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3492b-107">EXAMPLES</span></span>

### <span data-ttu-id="3492b-108">Exemplo 1: criar um mapeamento</span><span class="sxs-lookup"><span data-stu-id="3492b-108">Example 1: Create a mapping</span></span>
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

<span data-ttu-id="3492b-109">Criar um mapeamento</span><span class="sxs-lookup"><span data-stu-id="3492b-109">Create a mapping</span></span>

## <span data-ttu-id="3492b-110">OS</span><span class="sxs-lookup"><span data-stu-id="3492b-110">PARAMETERS</span></span>

### <span data-ttu-id="3492b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3492b-111">-AsJob</span></span>
<span data-ttu-id="3492b-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3492b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3492b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3492b-113">-DefaultProfile</span></span>
<span data-ttu-id="3492b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3492b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3492b-115">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="3492b-115">-FabricName</span></span>
<span data-ttu-id="3492b-116">Nome do tecido.</span><span class="sxs-lookup"><span data-stu-id="3492b-116">Fabric name.</span></span>

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

### <span data-ttu-id="3492b-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="3492b-117">-MappingName</span></span>
<span data-ttu-id="3492b-118">Nome do mapeamento do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="3492b-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="3492b-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3492b-119">-NoWait</span></span>
<span data-ttu-id="3492b-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3492b-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3492b-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="3492b-121">-PolicyId</span></span>
<span data-ttu-id="3492b-122">Política aplicável.</span><span class="sxs-lookup"><span data-stu-id="3492b-122">Applicable policy.</span></span>

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

### <span data-ttu-id="3492b-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="3492b-123">-ProtectionContainerName</span></span>
<span data-ttu-id="3492b-124">Nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="3492b-124">Protection container name.</span></span>

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

### <span data-ttu-id="3492b-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="3492b-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="3492b-126">Entrada específica do provedor para emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="3492b-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="3492b-127">Para construir, consulte a seção notas para propriedades PROVIDERSPECIFICINPUT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3492b-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3492b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3492b-128">-ResourceGroupName</span></span>
<span data-ttu-id="3492b-129">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="3492b-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="3492b-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3492b-130">-ResourceName</span></span>
<span data-ttu-id="3492b-131">O nome do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3492b-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="3492b-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3492b-132">-SubscriptionId</span></span>
<span data-ttu-id="3492b-133">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3492b-133">The subscription Id.</span></span>

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

### <span data-ttu-id="3492b-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="3492b-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="3492b-135">O nome exclusivo do contêiner de proteção de destino.</span><span class="sxs-lookup"><span data-stu-id="3492b-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="3492b-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3492b-136">-Confirm</span></span>
<span data-ttu-id="3492b-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3492b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3492b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3492b-138">-WhatIf</span></span>
<span data-ttu-id="3492b-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3492b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3492b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3492b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3492b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3492b-141">CommonParameters</span></span>
<span data-ttu-id="3492b-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3492b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3492b-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3492b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3492b-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3492b-144">INPUTS</span></span>

## <span data-ttu-id="3492b-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3492b-145">OUTPUTS</span></span>

### <span data-ttu-id="3492b-146">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3492b-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="3492b-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3492b-147">NOTES</span></span>

<span data-ttu-id="3492b-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3492b-148">ALIASES</span></span>

<span data-ttu-id="3492b-149">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="3492b-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3492b-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3492b-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3492b-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3492b-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3492b-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : entrada específica do provedor para emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="3492b-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="3492b-153">`[InstanceType <String>]`: O tipo de classe.</span><span class="sxs-lookup"><span data-stu-id="3492b-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="3492b-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3492b-154">RELATED LINKS</span></span>

