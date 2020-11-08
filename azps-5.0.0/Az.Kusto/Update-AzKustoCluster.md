---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117718"
---
# <span data-ttu-id="f407d-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="f407d-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="f407d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f407d-102">SYNOPSIS</span></span>
<span data-ttu-id="f407d-103">Atualizar um cluster do Kusto.</span><span class="sxs-lookup"><span data-stu-id="f407d-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="f407d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f407d-104">SYNTAX</span></span>

### <span data-ttu-id="f407d-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="f407d-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f407d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f407d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f407d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f407d-107">DESCRIPTION</span></span>
<span data-ttu-id="f407d-108">Atualizar um cluster do Kusto.</span><span class="sxs-lookup"><span data-stu-id="f407d-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="f407d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f407d-109">EXAMPLES</span></span>

### <span data-ttu-id="f407d-110">Exemplo 1: atualizar um cluster existente por nome</span><span class="sxs-lookup"><span data-stu-id="f407d-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="f407d-111">O comando acima atualiza a SKU do cluster Kusto "testnewkustocluster" encontrada no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="f407d-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="f407d-112">Exemplo 2: atualizar um cluster existente por nome</span><span class="sxs-lookup"><span data-stu-id="f407d-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="f407d-113">O comando acima atualiza o cluster "testnewkustocluster" localizado no grupo de recursos "testrg" com uma chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="f407d-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="f407d-114">OS</span><span class="sxs-lookup"><span data-stu-id="f407d-114">PARAMETERS</span></span>

### <span data-ttu-id="f407d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f407d-115">-AsJob</span></span>
<span data-ttu-id="f407d-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f407d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f407d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f407d-117">-DefaultProfile</span></span>
<span data-ttu-id="f407d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f407d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f407d-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f407d-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="f407d-120">Um valor booliano que indica se os discos do cluster estão criptografados.</span><span class="sxs-lookup"><span data-stu-id="f407d-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="f407d-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="f407d-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="f407d-122">Um valor booliano que indica se A criptografia dupla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f407d-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="f407d-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="f407d-123">-EnablePurge</span></span>
<span data-ttu-id="f407d-124">Um valor booliano que indica se as operações de limpeza estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="f407d-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="f407d-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="f407d-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="f407d-126">Um valor booliano que indica se a inclusão de streaming está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f407d-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="f407d-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f407d-127">-IdentityType</span></span>
<span data-ttu-id="f407d-128">O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="f407d-128">The identity type.</span></span>

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

### <span data-ttu-id="f407d-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f407d-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="f407d-130">A lista de identidades de usuário associadas ao cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f407d-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="f407d-131">As referências de chave de dicionário de identidade do usuário serão ARM IDs de recurso no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="f407d-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="f407d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f407d-132">-InputObject</span></span>
<span data-ttu-id="f407d-133">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f407d-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f407d-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="f407d-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="f407d-135">O nome da chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f407d-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="f407d-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="f407d-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="f407d-137">O URI do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f407d-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="f407d-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f407d-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="f407d-139">A versão da chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f407d-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="f407d-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="f407d-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="f407d-141">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="f407d-141">The list of language extensions.</span></span>
<span data-ttu-id="f407d-142">Para construir, consulte a seção notas para propriedades LANGUAGEEXTENSIONVALUE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f407d-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f407d-143">-Local</span><span class="sxs-lookup"><span data-stu-id="f407d-143">-Location</span></span>
<span data-ttu-id="f407d-144">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f407d-144">Resource location.</span></span>

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

### <span data-ttu-id="f407d-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="f407d-145">-Name</span></span>
<span data-ttu-id="f407d-146">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f407d-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f407d-147">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f407d-147">-NoWait</span></span>
<span data-ttu-id="f407d-148">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="f407d-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f407d-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="f407d-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="f407d-150">Um valor booliano que indica se o recurso de autoescala otimizado está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="f407d-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="f407d-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="f407d-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="f407d-152">Contagem máxima permitida de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="f407d-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="f407d-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="f407d-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="f407d-154">Contagem mínima permitida de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="f407d-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="f407d-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="f407d-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="f407d-156">A versão do modelo definida, por exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="f407d-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="f407d-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f407d-157">-ResourceGroupName</span></span>
<span data-ttu-id="f407d-158">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f407d-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f407d-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f407d-159">-SkuCapacity</span></span>
<span data-ttu-id="f407d-160">O número de instâncias do cluster.</span><span class="sxs-lookup"><span data-stu-id="f407d-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="f407d-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f407d-161">-SkuName</span></span>
<span data-ttu-id="f407d-162">Nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="f407d-162">SKU name.</span></span>

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

### <span data-ttu-id="f407d-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f407d-163">-SkuTier</span></span>
<span data-ttu-id="f407d-164">Nível de SKU.</span><span class="sxs-lookup"><span data-stu-id="f407d-164">SKU tier.</span></span>

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

### <span data-ttu-id="f407d-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f407d-165">-SubscriptionId</span></span>
<span data-ttu-id="f407d-166">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f407d-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f407d-167">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f407d-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f407d-168">-Marca</span><span class="sxs-lookup"><span data-stu-id="f407d-168">-Tag</span></span>
<span data-ttu-id="f407d-169">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="f407d-169">Resource tags.</span></span>

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

### <span data-ttu-id="f407d-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="f407d-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="f407d-171">Locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="f407d-171">The cluster's external tenants.</span></span>
<span data-ttu-id="f407d-172">Para construir, consulte a seção notas para propriedades TRUSTEDEXTERNALTENANT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f407d-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f407d-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="f407d-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="f407d-174">ID do recurso do endereço IP público do serviço de gerenciamento de dados.</span><span class="sxs-lookup"><span data-stu-id="f407d-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="f407d-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="f407d-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="f407d-176">ID do recurso do endereço IP público do serviço de mecanismo.</span><span class="sxs-lookup"><span data-stu-id="f407d-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="f407d-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="f407d-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="f407d-178">A ID do recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f407d-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="f407d-179">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f407d-179">-Confirm</span></span>
<span data-ttu-id="f407d-180">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f407d-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f407d-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f407d-181">-WhatIf</span></span>
<span data-ttu-id="f407d-182">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f407d-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f407d-183">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f407d-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f407d-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f407d-184">CommonParameters</span></span>
<span data-ttu-id="f407d-185">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f407d-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f407d-186">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f407d-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f407d-187">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f407d-187">INPUTS</span></span>

### <span data-ttu-id="f407d-188">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f407d-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f407d-189">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f407d-189">OUTPUTS</span></span>

### <span data-ttu-id="f407d-190">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="f407d-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="f407d-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f407d-191">NOTES</span></span>

<span data-ttu-id="f407d-192">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f407d-192">ALIASES</span></span>

<span data-ttu-id="f407d-193">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f407d-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f407d-194">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f407d-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f407d-195">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f407d-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f407d-196">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f407d-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f407d-197">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="f407d-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f407d-198">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f407d-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f407d-199">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="f407d-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f407d-200">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f407d-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f407d-201">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f407d-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f407d-202">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="f407d-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f407d-203">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="f407d-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f407d-204">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f407d-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f407d-205">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f407d-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f407d-206">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f407d-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="f407d-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="f407d-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="f407d-208">`[Name <LanguageExtensionName?>]`: O nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="f407d-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="f407d-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: os locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="f407d-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="f407d-210">`[Value <String>]`: GUID que representa um locatário externo.</span><span class="sxs-lookup"><span data-stu-id="f407d-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="f407d-211">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f407d-211">RELATED LINKS</span></span>

