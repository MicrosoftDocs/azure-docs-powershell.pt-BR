---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b868633f0217b2048f0a83641f678e9c092d21c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429804"
---
# <span data-ttu-id="60476-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="60476-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="60476-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60476-102">SYNOPSIS</span></span>
<span data-ttu-id="60476-103">Criar ou atualizar um cluster do Kusto.</span><span class="sxs-lookup"><span data-stu-id="60476-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="60476-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60476-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60476-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60476-105">DESCRIPTION</span></span>
<span data-ttu-id="60476-106">Criar ou atualizar um cluster do Kusto.</span><span class="sxs-lookup"><span data-stu-id="60476-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="60476-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60476-107">EXAMPLES</span></span>

### <span data-ttu-id="60476-108">Exemplo 1: criar um novo Kusto cluster</span><span class="sxs-lookup"><span data-stu-id="60476-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="60476-109">O comando acima cria um novo Kusto cluster chamado "testnewkustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="60476-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="60476-110">OS</span><span class="sxs-lookup"><span data-stu-id="60476-110">PARAMETERS</span></span>

### <span data-ttu-id="60476-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60476-111">-AsJob</span></span>
<span data-ttu-id="60476-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="60476-112">Run the command as a job</span></span>

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

### <span data-ttu-id="60476-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60476-113">-DefaultProfile</span></span>
<span data-ttu-id="60476-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60476-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60476-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="60476-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="60476-116">Um valor booliano que indica se os discos do cluster estão criptografados.</span><span class="sxs-lookup"><span data-stu-id="60476-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="60476-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="60476-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="60476-118">Um valor booliano que indica se A criptografia dupla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="60476-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="60476-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="60476-119">-EnablePurge</span></span>
<span data-ttu-id="60476-120">Um valor booliano que indica se as operações de limpeza estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="60476-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="60476-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="60476-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="60476-122">Um valor booliano que indica se a inclusão de streaming está habilitada.</span><span class="sxs-lookup"><span data-stu-id="60476-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="60476-123">-Enginetype</span><span class="sxs-lookup"><span data-stu-id="60476-123">-EngineType</span></span>
<span data-ttu-id="60476-124">O tipo de mecanismo</span><span class="sxs-lookup"><span data-stu-id="60476-124">The engine type</span></span>

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

### <span data-ttu-id="60476-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="60476-125">-IdentityType</span></span>
<span data-ttu-id="60476-126">O tipo de identidade gerenciada usado.</span><span class="sxs-lookup"><span data-stu-id="60476-126">The type of managed identity used.</span></span>
<span data-ttu-id="60476-127">O tipo ' SystemAssigned, userassigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="60476-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="60476-128">O tipo ' nenhum ' vai remover todas as identidades.</span><span class="sxs-lookup"><span data-stu-id="60476-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="60476-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="60476-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="60476-130">A lista de identidades de usuário associadas ao cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="60476-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="60476-131">As referências de chave de dicionário de identidade do usuário serão ARM IDs de recurso no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="60476-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="60476-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="60476-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="60476-133">O nome da chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="60476-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="60476-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="60476-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="60476-135">O URI do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="60476-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="60476-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="60476-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="60476-137">A versão da chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="60476-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="60476-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="60476-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="60476-139">A identidade atribuída ao usuário (ID do recurso ARM) que tem acesso à chave.</span><span class="sxs-lookup"><span data-stu-id="60476-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="60476-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="60476-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="60476-141">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="60476-141">The list of language extensions.</span></span>
<span data-ttu-id="60476-142">Para construir, consulte a seção notas para propriedades LANGUAGEEXTENSIONVALUE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="60476-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="60476-143">-Local</span><span class="sxs-lookup"><span data-stu-id="60476-143">-Location</span></span>
<span data-ttu-id="60476-144">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="60476-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="60476-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="60476-145">-Name</span></span>
<span data-ttu-id="60476-146">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="60476-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60476-147">-Nowait</span><span class="sxs-lookup"><span data-stu-id="60476-147">-NoWait</span></span>
<span data-ttu-id="60476-148">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="60476-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="60476-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="60476-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="60476-150">Um valor booliano que indica se o recurso de autoescala otimizado está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="60476-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="60476-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="60476-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="60476-152">Contagem máxima permitida de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="60476-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="60476-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="60476-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="60476-154">Contagem mínima permitida de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="60476-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="60476-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="60476-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="60476-156">A versão do modelo definida, por exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="60476-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="60476-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60476-157">-ResourceGroupName</span></span>
<span data-ttu-id="60476-158">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="60476-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="60476-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="60476-159">-SkuCapacity</span></span>
<span data-ttu-id="60476-160">O número de instâncias do cluster.</span><span class="sxs-lookup"><span data-stu-id="60476-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="60476-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="60476-161">-SkuName</span></span>
<span data-ttu-id="60476-162">Nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="60476-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60476-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="60476-163">-SkuTier</span></span>
<span data-ttu-id="60476-164">Nível de SKU.</span><span class="sxs-lookup"><span data-stu-id="60476-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60476-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60476-165">-SubscriptionId</span></span>
<span data-ttu-id="60476-166">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="60476-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="60476-167">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="60476-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="60476-168">-Marca</span><span class="sxs-lookup"><span data-stu-id="60476-168">-Tag</span></span>
<span data-ttu-id="60476-169">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="60476-169">Resource tags.</span></span>

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

### <span data-ttu-id="60476-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="60476-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="60476-171">Locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="60476-171">The cluster's external tenants.</span></span>
<span data-ttu-id="60476-172">Para construir, consulte a seção notas para propriedades TRUSTEDEXTERNALTENANT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="60476-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60476-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="60476-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="60476-174">ID do recurso do endereço IP público do serviço de gerenciamento de dados.</span><span class="sxs-lookup"><span data-stu-id="60476-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="60476-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="60476-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="60476-176">ID do recurso do endereço IP público do serviço de mecanismo.</span><span class="sxs-lookup"><span data-stu-id="60476-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="60476-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="60476-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="60476-178">A ID do recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="60476-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="60476-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="60476-179">-Zone</span></span>
<span data-ttu-id="60476-180">As zonas de disponibilidade do cluster.</span><span class="sxs-lookup"><span data-stu-id="60476-180">The availability zones of the cluster.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60476-181">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60476-181">-Confirm</span></span>
<span data-ttu-id="60476-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60476-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60476-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60476-183">-WhatIf</span></span>
<span data-ttu-id="60476-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60476-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60476-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60476-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60476-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60476-186">CommonParameters</span></span>
<span data-ttu-id="60476-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60476-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60476-188">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60476-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60476-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60476-189">INPUTS</span></span>

## <span data-ttu-id="60476-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60476-190">OUTPUTS</span></span>

### <span data-ttu-id="60476-191">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="60476-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="60476-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60476-192">NOTES</span></span>

<span data-ttu-id="60476-193">ALIASES</span><span class="sxs-lookup"><span data-stu-id="60476-193">ALIASES</span></span>

<span data-ttu-id="60476-194">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="60476-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60476-195">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="60476-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60476-196">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60476-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60476-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="60476-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="60476-198">`[Name <LanguageExtensionName?>]`: O nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="60476-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="60476-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: os locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="60476-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="60476-200">`[Value <String>]`: GUID que representa um locatário externo.</span><span class="sxs-lookup"><span data-stu-id="60476-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="60476-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60476-201">RELATED LINKS</span></span>

