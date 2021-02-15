---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111822"
---
# <span data-ttu-id="2b5ff-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="2b5ff-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="2b5ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="2b5ff-103">Atualizar um cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="2b5ff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b5ff-104">SYNTAX</span></span>

### <span data-ttu-id="2b5ff-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b5ff-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="2b5ff-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2b5ff-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="2b5ff-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b5ff-107">DESCRIPTION</span></span>
<span data-ttu-id="2b5ff-108">Atualizar um cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="2b5ff-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2b5ff-109">EXAMPLES</span></span>

### <span data-ttu-id="2b5ff-110">Exemplo 1: Atualizar um cluster existente por nome</span><span class="sxs-lookup"><span data-stu-id="2b5ff-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="2b5ff-111">O comando acima atualiza a sKU do cluster de Kusto "testnewkustocluster" encontrada no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="2b5ff-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="2b5ff-112">Exemplo 2: Atualizar um cluster existente por nome</span><span class="sxs-lookup"><span data-stu-id="2b5ff-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="2b5ff-113">O comando acima atualiza o cluster "testnewkustocluster" encontrado no grupo de recursos "testrg" com uma chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="2b5ff-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b5ff-114">PARAMETERS</span></span>

### <span data-ttu-id="2b5ff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b5ff-115">-AsJob</span></span>
<span data-ttu-id="2b5ff-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="2b5ff-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2b5ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b5ff-117">-DefaultProfile</span></span>
<span data-ttu-id="2b5ff-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b5ff-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2b5ff-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="2b5ff-120">Um valor boolano que indica se os discos do cluster são criptografados.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="2b5ff-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="2b5ff-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="2b5ff-122">Um valor boolano que indica se a criptografia dupla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="2b5ff-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="2b5ff-123">-EnablePurge</span></span>
<span data-ttu-id="2b5ff-124">Um valor boolano que indica se as operações de limpeza estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="2b5ff-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="2b5ff-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="2b5ff-126">Um valor boolano que indica se a ingestão de streaming está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="2b5ff-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="2b5ff-127">-EngineType</span></span>
<span data-ttu-id="2b5ff-128">O tipo de mecanismo</span><span class="sxs-lookup"><span data-stu-id="2b5ff-128">The engine type</span></span>

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

### <span data-ttu-id="2b5ff-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2b5ff-129">-IdentityType</span></span>
<span data-ttu-id="2b5ff-130">O tipo de identidade gerenciada usada.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-130">The type of managed identity used.</span></span>
<span data-ttu-id="2b5ff-131">O tipo "SystemAssigned, UserAssigned" inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="2b5ff-132">O tipo "Nenhum" removerá todas as identidades.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-132">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="2b5ff-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2b5ff-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="2b5ff-134">A lista de identidades de usuário associadas ao cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="2b5ff-135">As referências de chave do dicionário de identidade do usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="2b5ff-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b5ff-136">-InputObject</span></span>
<span data-ttu-id="2b5ff-137">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2b5ff-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="2b5ff-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="2b5ff-139">O nome da chave do cofre.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="2b5ff-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="2b5ff-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="2b5ff-141">O Uri do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="2b5ff-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="2b5ff-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="2b5ff-143">A versão da chave do cofre.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="2b5ff-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="2b5ff-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="2b5ff-145">A identidade atribuída pelo usuário (ID de recurso ARM) que tem acesso à chave.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="2b5ff-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="2b5ff-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="2b5ff-147">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-147">The list of language extensions.</span></span>
<span data-ttu-id="2b5ff-148">Para construir, confira a seção ANOTAÇÕES das propriedades LANGUAGEEXTENSIONVALUE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="2b5ff-149">-Local</span><span class="sxs-lookup"><span data-stu-id="2b5ff-149">-Location</span></span>
<span data-ttu-id="2b5ff-150">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-150">Resource location.</span></span>

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

### <span data-ttu-id="2b5ff-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b5ff-151">-Name</span></span>
<span data-ttu-id="2b5ff-152">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-152">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2b5ff-153">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2b5ff-153">-NoWait</span></span>
<span data-ttu-id="2b5ff-154">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="2b5ff-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2b5ff-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="2b5ff-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="2b5ff-156">Um valor boolano que indica se o recurso de escala automática otimizada está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="2b5ff-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="2b5ff-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="2b5ff-158">Contagem máxima de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-158">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="2b5ff-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="2b5ff-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="2b5ff-160">Contagem mínima de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-160">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="2b5ff-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="2b5ff-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="2b5ff-162">A versão do modelo definida, por exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-162">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="2b5ff-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b5ff-163">-ResourceGroupName</span></span>
<span data-ttu-id="2b5ff-164">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2b5ff-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2b5ff-165">-SkuCapacity</span></span>
<span data-ttu-id="2b5ff-166">O número de instâncias do cluster.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-166">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="2b5ff-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2b5ff-167">-SkuName</span></span>
<span data-ttu-id="2b5ff-168">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-168">SKU name.</span></span>

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

### <span data-ttu-id="2b5ff-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2b5ff-169">-SkuTier</span></span>
<span data-ttu-id="2b5ff-170">Camada SKU.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-170">SKU tier.</span></span>

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

### <span data-ttu-id="2b5ff-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b5ff-171">-SubscriptionId</span></span>
<span data-ttu-id="2b5ff-172">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2b5ff-173">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2b5ff-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b5ff-174">-Tag</span></span>
<span data-ttu-id="2b5ff-175">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-175">Resource tags.</span></span>

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

### <span data-ttu-id="2b5ff-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="2b5ff-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="2b5ff-177">Os locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-177">The cluster's external tenants.</span></span>
<span data-ttu-id="2b5ff-178">Para construir, confira a seção ANOTAÇÕES das propriedades TRUSTEDEXTERNALTENANT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2b5ff-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="2b5ff-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="2b5ff-180">ID do recurso de endereço IP público do serviço de gerenciamento de dados.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="2b5ff-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="2b5ff-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="2b5ff-182">ID do recurso de endereço IP público do serviço de mecanismo.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="2b5ff-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="2b5ff-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="2b5ff-184">A ID do recurso da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="2b5ff-185">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2b5ff-185">-Confirm</span></span>
<span data-ttu-id="2b5ff-186">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b5ff-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b5ff-187">-WhatIf</span></span>
<span data-ttu-id="2b5ff-188">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b5ff-189">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b5ff-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b5ff-190">CommonParameters</span></span>
<span data-ttu-id="2b5ff-191">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b5ff-192">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b5ff-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b5ff-193">Entradas</span><span class="sxs-lookup"><span data-stu-id="2b5ff-193">INPUTS</span></span>

### <span data-ttu-id="2b5ff-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2b5ff-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2b5ff-195">Saídas</span><span class="sxs-lookup"><span data-stu-id="2b5ff-195">OUTPUTS</span></span>

### <span data-ttu-id="2b5ff-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="2b5ff-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="2b5ff-197">Notas</span><span class="sxs-lookup"><span data-stu-id="2b5ff-197">NOTES</span></span>

<span data-ttu-id="2b5ff-198">Aliases</span><span class="sxs-lookup"><span data-stu-id="2b5ff-198">ALIASES</span></span>

<span data-ttu-id="2b5ff-199">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="2b5ff-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2b5ff-200">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b5ff-201">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2b5ff-202">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="2b5ff-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2b5ff-203">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2b5ff-204">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2b5ff-205">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2b5ff-206">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2b5ff-207">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="2b5ff-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2b5ff-208">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2b5ff-209">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2b5ff-210">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2b5ff-211">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2b5ff-212">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="2b5ff-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="2b5ff-214">`[Name <LanguageExtensionName?>]`: o nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="2b5ff-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: os locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="2b5ff-216">`[Value <String>]`: GUID representando um locatário externo.</span><span class="sxs-lookup"><span data-stu-id="2b5ff-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="2b5ff-217">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b5ff-217">RELATED LINKS</span></span>

