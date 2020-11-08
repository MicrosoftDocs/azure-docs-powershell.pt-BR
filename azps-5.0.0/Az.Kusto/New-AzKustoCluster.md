---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124938"
---
# <span data-ttu-id="71a0e-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="71a0e-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="71a0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="71a0e-103">Criar ou atualizar um cluster do Kusto.</span><span class="sxs-lookup"><span data-stu-id="71a0e-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="71a0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71a0e-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71a0e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71a0e-105">DESCRIPTION</span></span>
<span data-ttu-id="71a0e-106">Criar ou atualizar um cluster do Kusto.</span><span class="sxs-lookup"><span data-stu-id="71a0e-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="71a0e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71a0e-107">EXAMPLES</span></span>

### <span data-ttu-id="71a0e-108">Exemplo 1: criar um novo Kusto cluster</span><span class="sxs-lookup"><span data-stu-id="71a0e-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="71a0e-109">O comando acima cria um novo Kusto cluster chamado "testnewkustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="71a0e-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="71a0e-110">OS</span><span class="sxs-lookup"><span data-stu-id="71a0e-110">PARAMETERS</span></span>

### <span data-ttu-id="71a0e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71a0e-111">-AsJob</span></span>
<span data-ttu-id="71a0e-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="71a0e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="71a0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a0e-113">-DefaultProfile</span></span>
<span data-ttu-id="71a0e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71a0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71a0e-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="71a0e-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="71a0e-116">Um valor booliano que indica se os discos do cluster estão criptografados.</span><span class="sxs-lookup"><span data-stu-id="71a0e-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="71a0e-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="71a0e-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="71a0e-118">Um valor booliano que indica se A criptografia dupla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="71a0e-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="71a0e-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="71a0e-119">-EnablePurge</span></span>
<span data-ttu-id="71a0e-120">Um valor booliano que indica se as operações de limpeza estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="71a0e-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="71a0e-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="71a0e-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="71a0e-122">Um valor booliano que indica se a inclusão de streaming está habilitada.</span><span class="sxs-lookup"><span data-stu-id="71a0e-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="71a0e-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="71a0e-123">-IdentityType</span></span>
<span data-ttu-id="71a0e-124">O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="71a0e-124">The identity type.</span></span>

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

### <span data-ttu-id="71a0e-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="71a0e-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="71a0e-126">A lista de identidades de usuário associadas ao cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="71a0e-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="71a0e-127">As referências de chave de dicionário de identidade do usuário serão ARM IDs de recurso no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="71a0e-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="71a0e-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="71a0e-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="71a0e-129">O nome da chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="71a0e-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="71a0e-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="71a0e-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="71a0e-131">O URI do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="71a0e-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="71a0e-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="71a0e-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="71a0e-133">A versão da chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="71a0e-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="71a0e-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="71a0e-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="71a0e-135">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="71a0e-135">The list of language extensions.</span></span>
<span data-ttu-id="71a0e-136">Para construir, consulte a seção notas para propriedades LANGUAGEEXTENSIONVALUE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="71a0e-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="71a0e-137">-Local</span><span class="sxs-lookup"><span data-stu-id="71a0e-137">-Location</span></span>
<span data-ttu-id="71a0e-138">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="71a0e-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="71a0e-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="71a0e-139">-Name</span></span>
<span data-ttu-id="71a0e-140">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="71a0e-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="71a0e-141">-Nowait</span><span class="sxs-lookup"><span data-stu-id="71a0e-141">-NoWait</span></span>
<span data-ttu-id="71a0e-142">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="71a0e-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="71a0e-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="71a0e-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="71a0e-144">Um valor booliano que indica se o recurso de autoescala otimizado está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="71a0e-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="71a0e-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="71a0e-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="71a0e-146">Contagem máxima permitida de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="71a0e-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="71a0e-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="71a0e-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="71a0e-148">Contagem mínima permitida de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="71a0e-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="71a0e-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="71a0e-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="71a0e-150">A versão do modelo definida, por exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="71a0e-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="71a0e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a0e-151">-ResourceGroupName</span></span>
<span data-ttu-id="71a0e-152">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="71a0e-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="71a0e-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="71a0e-153">-SkuCapacity</span></span>
<span data-ttu-id="71a0e-154">O número de instâncias do cluster.</span><span class="sxs-lookup"><span data-stu-id="71a0e-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="71a0e-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="71a0e-155">-SkuName</span></span>
<span data-ttu-id="71a0e-156">Nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="71a0e-156">SKU name.</span></span>

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

### <span data-ttu-id="71a0e-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="71a0e-157">-SkuTier</span></span>
<span data-ttu-id="71a0e-158">Nível de SKU.</span><span class="sxs-lookup"><span data-stu-id="71a0e-158">SKU tier.</span></span>

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

### <span data-ttu-id="71a0e-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71a0e-159">-SubscriptionId</span></span>
<span data-ttu-id="71a0e-160">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="71a0e-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="71a0e-161">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="71a0e-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="71a0e-162">-Marca</span><span class="sxs-lookup"><span data-stu-id="71a0e-162">-Tag</span></span>
<span data-ttu-id="71a0e-163">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="71a0e-163">Resource tags.</span></span>

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

### <span data-ttu-id="71a0e-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="71a0e-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="71a0e-165">Locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="71a0e-165">The cluster's external tenants.</span></span>
<span data-ttu-id="71a0e-166">Para construir, consulte a seção notas para propriedades TRUSTEDEXTERNALTENANT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="71a0e-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="71a0e-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="71a0e-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="71a0e-168">ID do recurso do endereço IP público do serviço de gerenciamento de dados.</span><span class="sxs-lookup"><span data-stu-id="71a0e-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="71a0e-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="71a0e-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="71a0e-170">ID do recurso do endereço IP público do serviço de mecanismo.</span><span class="sxs-lookup"><span data-stu-id="71a0e-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="71a0e-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="71a0e-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="71a0e-172">A ID do recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="71a0e-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="71a0e-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="71a0e-173">-Zone</span></span>
<span data-ttu-id="71a0e-174">As zonas de disponibilidade do cluster.</span><span class="sxs-lookup"><span data-stu-id="71a0e-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="71a0e-175">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71a0e-175">-Confirm</span></span>
<span data-ttu-id="71a0e-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71a0e-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a0e-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a0e-177">-WhatIf</span></span>
<span data-ttu-id="71a0e-178">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71a0e-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a0e-179">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71a0e-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a0e-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a0e-180">CommonParameters</span></span>
<span data-ttu-id="71a0e-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71a0e-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a0e-182">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71a0e-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a0e-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71a0e-183">INPUTS</span></span>

## <span data-ttu-id="71a0e-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71a0e-184">OUTPUTS</span></span>

### <span data-ttu-id="71a0e-185">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="71a0e-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="71a0e-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71a0e-186">NOTES</span></span>

<span data-ttu-id="71a0e-187">ALIASES</span><span class="sxs-lookup"><span data-stu-id="71a0e-187">ALIASES</span></span>

<span data-ttu-id="71a0e-188">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="71a0e-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71a0e-189">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="71a0e-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71a0e-190">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71a0e-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71a0e-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="71a0e-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="71a0e-192">`[Name <LanguageExtensionName?>]`: O nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="71a0e-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="71a0e-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: os locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="71a0e-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="71a0e-194">`[Value <String>]`: GUID que representa um locatário externo.</span><span class="sxs-lookup"><span data-stu-id="71a0e-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="71a0e-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71a0e-195">RELATED LINKS</span></span>

