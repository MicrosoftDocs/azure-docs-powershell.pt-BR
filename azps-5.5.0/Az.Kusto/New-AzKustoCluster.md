---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b868633f0217b2048f0a83641f678e9c092d21c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118947"
---
# <span data-ttu-id="85f70-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="85f70-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="85f70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85f70-102">SYNOPSIS</span></span>
<span data-ttu-id="85f70-103">Criar ou atualizar um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="85f70-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="85f70-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85f70-104">SYNTAX</span></span>

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

## <span data-ttu-id="85f70-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="85f70-105">DESCRIPTION</span></span>
<span data-ttu-id="85f70-106">Criar ou atualizar um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="85f70-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="85f70-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="85f70-107">EXAMPLES</span></span>

### <span data-ttu-id="85f70-108">Exemplo 1: Criar um novo cluster de Kusto</span><span class="sxs-lookup"><span data-stu-id="85f70-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="85f70-109">O comando acima cria um novo cluster Kusto chamado "testnewkustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="85f70-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="85f70-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85f70-110">PARAMETERS</span></span>

### <span data-ttu-id="85f70-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85f70-111">-AsJob</span></span>
<span data-ttu-id="85f70-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="85f70-112">Run the command as a job</span></span>

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

### <span data-ttu-id="85f70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f70-113">-DefaultProfile</span></span>
<span data-ttu-id="85f70-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85f70-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85f70-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="85f70-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="85f70-116">Um valor boolano que indica se os discos do cluster são criptografados.</span><span class="sxs-lookup"><span data-stu-id="85f70-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="85f70-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="85f70-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="85f70-118">Um valor boolano que indica se a criptografia dupla está habilitada.</span><span class="sxs-lookup"><span data-stu-id="85f70-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="85f70-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="85f70-119">-EnablePurge</span></span>
<span data-ttu-id="85f70-120">Um valor boolano que indica se as operações de limpeza estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="85f70-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="85f70-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="85f70-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="85f70-122">Um valor boolano que indica se a ingestão de streaming está habilitada.</span><span class="sxs-lookup"><span data-stu-id="85f70-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="85f70-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="85f70-123">-EngineType</span></span>
<span data-ttu-id="85f70-124">O tipo de mecanismo</span><span class="sxs-lookup"><span data-stu-id="85f70-124">The engine type</span></span>

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

### <span data-ttu-id="85f70-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="85f70-125">-IdentityType</span></span>
<span data-ttu-id="85f70-126">O tipo de identidade gerenciada usada.</span><span class="sxs-lookup"><span data-stu-id="85f70-126">The type of managed identity used.</span></span>
<span data-ttu-id="85f70-127">O tipo "SystemAssigned, UserAssigned" inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="85f70-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="85f70-128">O tipo "Nenhum" removerá todas as identidades.</span><span class="sxs-lookup"><span data-stu-id="85f70-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="85f70-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="85f70-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="85f70-130">A lista de identidades de usuário associadas ao cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="85f70-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="85f70-131">As referências de chave do dicionário de identidade do usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="85f70-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="85f70-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="85f70-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="85f70-133">O nome da chave do cofre.</span><span class="sxs-lookup"><span data-stu-id="85f70-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="85f70-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="85f70-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="85f70-135">O Uri do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="85f70-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="85f70-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="85f70-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="85f70-137">A versão da chave do cofre.</span><span class="sxs-lookup"><span data-stu-id="85f70-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="85f70-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="85f70-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="85f70-139">A identidade atribuída pelo usuário (ID de recurso ARM) que tem acesso à chave.</span><span class="sxs-lookup"><span data-stu-id="85f70-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="85f70-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="85f70-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="85f70-141">A lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="85f70-141">The list of language extensions.</span></span>
<span data-ttu-id="85f70-142">Para construir, confira a seção ANOTAÇÕES das propriedades LANGUAGEEXTENSIONVALUE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="85f70-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="85f70-143">-Local</span><span class="sxs-lookup"><span data-stu-id="85f70-143">-Location</span></span>
<span data-ttu-id="85f70-144">A localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="85f70-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="85f70-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="85f70-145">-Name</span></span>
<span data-ttu-id="85f70-146">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="85f70-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="85f70-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="85f70-147">-NoWait</span></span>
<span data-ttu-id="85f70-148">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="85f70-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="85f70-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="85f70-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="85f70-150">Um valor boolano que indica se o recurso de escala automática otimizada está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="85f70-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="85f70-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="85f70-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="85f70-152">Contagem máxima de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="85f70-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="85f70-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="85f70-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="85f70-154">Contagem mínima de instâncias permitidas.</span><span class="sxs-lookup"><span data-stu-id="85f70-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="85f70-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="85f70-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="85f70-156">A versão do modelo definida, por exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="85f70-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="85f70-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f70-157">-ResourceGroupName</span></span>
<span data-ttu-id="85f70-158">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="85f70-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="85f70-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="85f70-159">-SkuCapacity</span></span>
<span data-ttu-id="85f70-160">O número de instâncias do cluster.</span><span class="sxs-lookup"><span data-stu-id="85f70-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="85f70-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="85f70-161">-SkuName</span></span>
<span data-ttu-id="85f70-162">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="85f70-162">SKU name.</span></span>

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

### <span data-ttu-id="85f70-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="85f70-163">-SkuTier</span></span>
<span data-ttu-id="85f70-164">Camada SKU.</span><span class="sxs-lookup"><span data-stu-id="85f70-164">SKU tier.</span></span>

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

### <span data-ttu-id="85f70-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85f70-165">-SubscriptionId</span></span>
<span data-ttu-id="85f70-166">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="85f70-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="85f70-167">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="85f70-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="85f70-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="85f70-168">-Tag</span></span>
<span data-ttu-id="85f70-169">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="85f70-169">Resource tags.</span></span>

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

### <span data-ttu-id="85f70-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="85f70-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="85f70-171">Os locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="85f70-171">The cluster's external tenants.</span></span>
<span data-ttu-id="85f70-172">Para construir, confira a seção ANOTAÇÕES das propriedades TRUSTEDEXTERNALTENANT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="85f70-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="85f70-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="85f70-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="85f70-174">ID do recurso de endereço IP público do serviço de gerenciamento de dados.</span><span class="sxs-lookup"><span data-stu-id="85f70-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="85f70-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="85f70-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="85f70-176">ID do recurso de endereço IP público do serviço de mecanismo.</span><span class="sxs-lookup"><span data-stu-id="85f70-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="85f70-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="85f70-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="85f70-178">A ID do recurso da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="85f70-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="85f70-179">-Zona</span><span class="sxs-lookup"><span data-stu-id="85f70-179">-Zone</span></span>
<span data-ttu-id="85f70-180">As zonas de disponibilidade do cluster.</span><span class="sxs-lookup"><span data-stu-id="85f70-180">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="85f70-181">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="85f70-181">-Confirm</span></span>
<span data-ttu-id="85f70-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f70-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85f70-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85f70-183">-WhatIf</span></span>
<span data-ttu-id="85f70-184">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="85f70-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85f70-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85f70-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85f70-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f70-186">CommonParameters</span></span>
<span data-ttu-id="85f70-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f70-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f70-188">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85f70-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f70-189">Entradas</span><span class="sxs-lookup"><span data-stu-id="85f70-189">INPUTS</span></span>

## <span data-ttu-id="85f70-190">Saídas</span><span class="sxs-lookup"><span data-stu-id="85f70-190">OUTPUTS</span></span>

### <span data-ttu-id="85f70-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="85f70-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="85f70-192">Notas</span><span class="sxs-lookup"><span data-stu-id="85f70-192">NOTES</span></span>

<span data-ttu-id="85f70-193">Aliases</span><span class="sxs-lookup"><span data-stu-id="85f70-193">ALIASES</span></span>

<span data-ttu-id="85f70-194">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="85f70-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85f70-195">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="85f70-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85f70-196">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85f70-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85f70-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: a lista de extensões de idioma.</span><span class="sxs-lookup"><span data-stu-id="85f70-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="85f70-198">`[Name <LanguageExtensionName?>]`: o nome da extensão do idioma.</span><span class="sxs-lookup"><span data-stu-id="85f70-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="85f70-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: os locatários externos do cluster.</span><span class="sxs-lookup"><span data-stu-id="85f70-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="85f70-200">`[Value <String>]`: GUID representando um locatário externo.</span><span class="sxs-lookup"><span data-stu-id="85f70-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="85f70-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85f70-201">RELATED LINKS</span></span>

