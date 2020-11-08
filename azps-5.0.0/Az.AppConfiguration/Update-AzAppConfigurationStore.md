---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 944241dc7434646272c7149d81b380996e71db8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116441"
---
# <span data-ttu-id="8f024-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="8f024-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="8f024-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f024-102">SYNOPSIS</span></span>
<span data-ttu-id="8f024-103">Atualiza um repositório de configuração com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="8f024-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="8f024-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f024-104">SYNTAX</span></span>

### <span data-ttu-id="8f024-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="8f024-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f024-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8f024-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8f024-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f024-107">DESCRIPTION</span></span>
<span data-ttu-id="8f024-108">Atualiza um repositório de configuração com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="8f024-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="8f024-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f024-109">EXAMPLES</span></span>

### <span data-ttu-id="8f024-110">Exemplo 1: habilitar a criptografia de dados da App conifguration Store por identidade gerenciada atribuída pelo sistema</span><span class="sxs-lookup"><span data-stu-id="8f024-110">Example 1: Enable data encryption of the app conifguration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="8f024-111">Esse comando habilita a criptografia de dados por uma chave armazenada no cofre de chaves do Azure usando uma identidade gerenciada atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="8f024-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="8f024-112">O cofre deve ter uma exclusão de exclusão flexível e proteção de limpeza, e a identidade gerenciada deve ter essas permissões de chave: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="8f024-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="8f024-113">Exemplo 2: habilitar a criptografia de dados do App conifguration Store por identidade gerenciada atribuída pelo usuário</span><span class="sxs-lookup"><span data-stu-id="8f024-113">Example 2: Enable data encryption of the app conifguration store by user-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="8f024-114">Esse comando habilita a criptografia de dados por uma chave armazenada no cofre de chaves do Azure usando uma identidade gerenciada atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8f024-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="8f024-115">A identidade atribuída pelo usuário deve ter sido definida com `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="8f024-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="8f024-116">O cofre deve ter uma exclusão de exclusão flexível e proteção de limpeza, e a identidade gerenciada deve ter essas permissões de chave: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="8f024-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="8f024-117">Exemplo 3: desabilitar a criptografia de uma loja do aplicativo conifguration.</span><span class="sxs-lookup"><span data-stu-id="8f024-117">Example 3: Disable encryption of an app conifguration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="8f024-118">Esse comando desabilita a criptografia de uma loja de aplicativos conifguration.</span><span class="sxs-lookup"><span data-stu-id="8f024-118">This command disables encryption of an app conifguration store.</span></span>

### <span data-ttu-id="8f024-119">Exemplo 3: Atualize a SKU e a marca de um app conifguration Store por pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f024-119">Example 3: Update sku and tag of an app conifguration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="8f024-120">Esse comando atualiza a SKU e a marca de um app conifguration Store por pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f024-120">This command updates sku and tag of an app conifguration store by pipeline.</span></span>

## <span data-ttu-id="8f024-121">OS</span><span class="sxs-lookup"><span data-stu-id="8f024-121">PARAMETERS</span></span>

### <span data-ttu-id="8f024-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f024-122">-AsJob</span></span>
<span data-ttu-id="8f024-123">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8f024-123">Run the command as a job</span></span>

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

### <span data-ttu-id="8f024-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f024-124">-DefaultProfile</span></span>
<span data-ttu-id="8f024-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f024-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f024-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="8f024-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="8f024-127">O URI da chave do cofre de chaves usada para criptografar dados.</span><span class="sxs-lookup"><span data-stu-id="8f024-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="8f024-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8f024-128">-IdentityType</span></span>
<span data-ttu-id="8f024-129">O tipo de identidade gerenciada usado.</span><span class="sxs-lookup"><span data-stu-id="8f024-129">The type of managed identity used.</span></span>
<span data-ttu-id="8f024-130">O tipo ' SystemAssignedAndUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8f024-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="8f024-131">O tipo ' nenhum ' removerá todas as identidades.</span><span class="sxs-lookup"><span data-stu-id="8f024-131">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f024-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f024-132">-InputObject</span></span>
<span data-ttu-id="8f024-133">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8f024-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f024-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="8f024-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="8f024-135">A ID do cliente da identidade que será usada para acessar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8f024-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="8f024-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f024-136">-Name</span></span>
<span data-ttu-id="8f024-137">O nome do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="8f024-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="8f024-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8f024-138">-NoWait</span></span>
<span data-ttu-id="8f024-139">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="8f024-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f024-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f024-140">-ResourceGroupName</span></span>
<span data-ttu-id="8f024-141">O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="8f024-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="8f024-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="8f024-142">-Sku</span></span>
<span data-ttu-id="8f024-143">O nome do SKU do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="8f024-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="8f024-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f024-144">-SubscriptionId</span></span>
<span data-ttu-id="8f024-145">A ID da assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f024-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="8f024-146">-Marca</span><span class="sxs-lookup"><span data-stu-id="8f024-146">-Tag</span></span>
<span data-ttu-id="8f024-147">As marcas de recurso ARM.</span><span class="sxs-lookup"><span data-stu-id="8f024-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="8f024-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8f024-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="8f024-149">A lista de identidades atribuídas pelo usuário associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="8f024-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="8f024-150">As chaves de dicionário de identidade atribuídas pelo usuário serão as IDs de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="8f024-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="8f024-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f024-151">-Confirm</span></span>
<span data-ttu-id="8f024-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f024-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f024-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f024-153">-WhatIf</span></span>
<span data-ttu-id="8f024-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f024-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f024-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f024-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f024-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f024-156">CommonParameters</span></span>
<span data-ttu-id="8f024-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f024-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f024-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f024-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f024-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f024-159">INPUTS</span></span>

### <span data-ttu-id="8f024-160">Microsoft. Azure. PowerShell. cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="8f024-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="8f024-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f024-161">OUTPUTS</span></span>

### <span data-ttu-id="8f024-162">Microsoft. Azure. PowerShell. cmdlets. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="8f024-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="8f024-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f024-163">NOTES</span></span>

<span data-ttu-id="8f024-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8f024-164">ALIASES</span></span>

<span data-ttu-id="8f024-165">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="8f024-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f024-166">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8f024-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f024-167">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f024-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f024-168">INPUTobject <IAppConfigurationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8f024-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f024-169">`[ConfigStoreName <String>]`: O nome do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="8f024-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="8f024-170">`[GroupName <String>]`: O nome do grupo de recursos de link privado.</span><span class="sxs-lookup"><span data-stu-id="8f024-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="8f024-171">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8f024-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f024-172">`[PrivateEndpointConnectionName <String>]`: Nome da conexão de ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="8f024-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="8f024-173">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="8f024-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="8f024-174">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f024-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="8f024-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f024-175">RELATED LINKS</span></span>



<span data-ttu-id="8f024-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="8f024-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

