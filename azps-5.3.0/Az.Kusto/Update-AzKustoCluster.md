---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272761"
---
# <span data-ttu-id="ce7e3-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="ce7e3-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="ce7e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7e3-103">Atualizar um cluster do Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="ce7e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce7e3-104">SYNTAX</span></span>

### <span data-ttu-id="ce7e3-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce7e3-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce7e3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ce7e3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce7e3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce7e3-107">DESCRIPTION</span></span>
<span data-ttu-id="ce7e3-108">Atualizar um cluster do Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="ce7e3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce7e3-109">EXAMPLES</span></span>

### <span data-ttu-id="ce7e3-110">Exemplo 1: atualizar um cluster existente por nome</span><span class="sxs-lookup"><span data-stu-id="ce7e3-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="ce7e3-111">O comando acima atualiza a SKU do cluster Kusto "testnewkustocluster" encontrada no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="ce7e3-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ce7e3-112">Exemplo 2: atualizar um cluster existente por nome</span><span class="sxs-lookup"><span data-stu-id="ce7e3-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="ce7e3-113">O comando acima atualiza o cluster "testnewkustocluster" localizado no grupo de recursos "testrg" com uma chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="ce7e3-114">OS</span><span class="sxs-lookup"><span data-stu-id="ce7e3-114">PARAMETERS</span></span>

### <span data-ttu-id="ce7e3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce7e3-115">-AsJob</span></span>
<span data-ttu-id="ce7e3-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ce7e3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ce7e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7e3-117">-DefaultProfile</span></span>
<span data-ttu-id="ce7e3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce7e3-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ce7e3-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="ce7e3-120">Um valor booliano que indica se os discos do cluster estão criptografados.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="ce7e3-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="ce7e3-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="ce7e3-122">Um valor booliano que indica se A criptografia dupla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="ce7e3-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="ce7e3-123">-EnablePurge</span></span>
<span data-ttu-id="ce7e3-124">Um valor booliano que indica se as operações de limpeza estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="ce7e3-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="ce7e3-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="ce7e3-126">Um valor booliano que indica se a inclusão de streaming está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="ce7e3-127">-Enginetype</span><span class="sxs-lookup"><span data-stu-id="ce7e3-127">-EngineType</span></span>
<span data-ttu-id="ce7e3-128">O tipo de mecanismo</span><span class="sxs-lookup"><span data-stu-id="ce7e3-128">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ce7e3-129">-IdentityType</span></span>
<span data-ttu-id="ce7e3-130">O tipo de identidade gerenciada usado.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-130">The type of managed identity used.</span></span>
<span data-ttu-id="ce7e3-131">O tipo ' SystemAssigned, userassigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="ce7e3-132">O tipo ' nenhum ' vai remover todas as identidades.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-132">The type 'None' will remove all identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ce7e3-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="ce7e3-134">A lista de identidades de usuário associadas ao cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="ce7e3-135">As referências de chave de dicionário de identidade do usuário serão ARM IDs de recurso no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce7e3-136">-InputObject</span></span>
<span data-ttu-id="ce7e3-137">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="ce7e3-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="ce7e3-139">O nome da chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="ce7e3-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ce7e3-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="ce7e3-141">O URI do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="ce7e3-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ce7e3-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="ce7e3-143">A versão da chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="ce7e3-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="ce7e3-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="ce7e3-145">A identidade atribuída ao usuário (ID do recurso ARM) que tem acesso à chave.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="ce7e3-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="ce7e3-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="ce7e3-147">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-147">The list of language extensions.</span></span>
<span data-ttu-id="ce7e3-148">Para construir, consulte a seção notas para propriedades LANGUAGEEXTENSIONVALUE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-149">-Local</span><span class="sxs-lookup"><span data-stu-id="ce7e3-149">-Location</span></span>
<span data-ttu-id="ce7e3-150">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-150">Resource location.</span></span>

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

### <span data-ttu-id="ce7e3-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce7e3-151">-Name</span></span>
<span data-ttu-id="ce7e3-152">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-152">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-153">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ce7e3-153">-NoWait</span></span>
<span data-ttu-id="ce7e3-154">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ce7e3-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ce7e3-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="ce7e3-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="ce7e3-156">Um valor booliano que indica se o recurso de autoescala otimizado está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="ce7e3-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="ce7e3-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="ce7e3-158">Contagem máxima permitida de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-158">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="ce7e3-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="ce7e3-160">Contagem mínima permitida de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-160">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="ce7e3-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="ce7e3-162">A versão do modelo definida, por exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-162">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce7e3-163">-ResourceGroupName</span></span>
<span data-ttu-id="ce7e3-164">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ce7e3-165">-SkuCapacity</span></span>
<span data-ttu-id="ce7e3-166">O número de instâncias do cluster.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-166">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ce7e3-167">-SkuName</span></span>
<span data-ttu-id="ce7e3-168">Nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-168">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ce7e3-169">-SkuTier</span></span>
<span data-ttu-id="ce7e3-170">Nível de SKU.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-170">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce7e3-171">-SubscriptionId</span></span>
<span data-ttu-id="ce7e3-172">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ce7e3-173">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-174">-Marca</span><span class="sxs-lookup"><span data-stu-id="ce7e3-174">-Tag</span></span>
<span data-ttu-id="ce7e3-175">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-175">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="ce7e3-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="ce7e3-177">Locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-177">The cluster's external tenants.</span></span>
<span data-ttu-id="ce7e3-178">Para construir, consulte a seção notas para propriedades TRUSTEDEXTERNALTENANT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7e3-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="ce7e3-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="ce7e3-180">ID do recurso do endereço IP público do serviço de gerenciamento de dados.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="ce7e3-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="ce7e3-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="ce7e3-182">ID do recurso do endereço IP público do serviço de mecanismo.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="ce7e3-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="ce7e3-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="ce7e3-184">A ID do recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="ce7e3-185">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce7e3-185">-Confirm</span></span>
<span data-ttu-id="ce7e3-186">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce7e3-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce7e3-187">-WhatIf</span></span>
<span data-ttu-id="ce7e3-188">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce7e3-189">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce7e3-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7e3-190">CommonParameters</span></span>
<span data-ttu-id="ce7e3-191">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7e3-192">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce7e3-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7e3-193">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce7e3-193">INPUTS</span></span>

### <span data-ttu-id="ce7e3-194">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ce7e3-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ce7e3-195">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce7e3-195">OUTPUTS</span></span>

### <span data-ttu-id="ce7e3-196">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="ce7e3-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="ce7e3-197">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce7e3-197">NOTES</span></span>

<span data-ttu-id="ce7e3-198">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ce7e3-198">ALIASES</span></span>

<span data-ttu-id="ce7e3-199">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="ce7e3-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce7e3-200">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce7e3-201">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce7e3-202">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="ce7e3-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce7e3-203">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ce7e3-204">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ce7e3-205">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ce7e3-206">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ce7e3-207">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ce7e3-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce7e3-208">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ce7e3-209">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ce7e3-210">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ce7e3-211">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ce7e3-212">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="ce7e3-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="ce7e3-214">`[Name <LanguageExtensionName?>]`: O nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="ce7e3-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: os locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="ce7e3-216">`[Value <String>]`: GUID que representa um locatário externo.</span><span class="sxs-lookup"><span data-stu-id="ce7e3-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="ce7e3-217">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce7e3-217">RELATED LINKS</span></span>

