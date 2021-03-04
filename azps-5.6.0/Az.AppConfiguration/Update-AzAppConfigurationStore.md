---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: b8297580f088678f1fdd61b8bff670adb03d2bcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887049"
---
# <span data-ttu-id="4847f-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="4847f-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="4847f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4847f-102">SYNOPSIS</span></span>
<span data-ttu-id="4847f-103">Atualiza um armazenamento de configuração com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="4847f-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="4847f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4847f-104">SYNTAX</span></span>

### <span data-ttu-id="4847f-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4847f-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4847f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4847f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4847f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4847f-107">DESCRIPTION</span></span>
<span data-ttu-id="4847f-108">Atualiza um armazenamento de configuração com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="4847f-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="4847f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4847f-109">EXAMPLES</span></span>

### <span data-ttu-id="4847f-110">Exemplo 1: Habilitar a criptografia de dados do armazenamento de configuração do aplicativo por identidade gerenciada atribuída pelo sistema</span><span class="sxs-lookup"><span data-stu-id="4847f-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4847f-111">Esse comando habilita a criptografia de dados por uma chave armazenada no Azure Key Vault usando uma identidade gerenciada atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="4847f-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="4847f-112">O cofre deve ter habilitado a exclusão suave e a proteção contra limpeza, e a identidade gerenciada deve ter essas permissões principais: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="4847f-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="4847f-113">Exemplo 2: Habilitar a criptografia de dados do armazenamento de configuração do aplicativo por identidade gerenciada atribuída pelo usuário</span><span class="sxs-lookup"><span data-stu-id="4847f-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="4847f-114">Esse comando habilita a criptografia de dados por uma chave armazenada no Azure Key Vault usando uma identidade gerenciada atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4847f-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="4847f-115">A identidade atribuída pelo usuário deve ter sido definida com `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="4847f-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="4847f-116">O cofre deve ter habilitado a exclusão suave e a proteção contra limpeza, e a identidade gerenciada deve ter essas permissões principais: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="4847f-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="4847f-117">Exemplo 3: Desabilitar a criptografia de um armazenamento de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4847f-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4847f-118">Esse comando desabilita a criptografia de um armazenamento de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4847f-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="4847f-119">Exemplo 3: Atualizar sku e marca de um armazenamento de configuração de aplicativo por pipeline.</span><span class="sxs-lookup"><span data-stu-id="4847f-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4847f-120">Este comando atualiza sku e marca de um armazenamento de configuração de aplicativo por pipeline.</span><span class="sxs-lookup"><span data-stu-id="4847f-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="4847f-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4847f-121">PARAMETERS</span></span>

### <span data-ttu-id="4847f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4847f-122">-AsJob</span></span>
<span data-ttu-id="4847f-123">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="4847f-123">Run the command as a job</span></span>

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

### <span data-ttu-id="4847f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4847f-124">-DefaultProfile</span></span>
<span data-ttu-id="4847f-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4847f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4847f-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="4847f-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="4847f-127">O URI da chave de cofre de chaves usada para criptografar dados.</span><span class="sxs-lookup"><span data-stu-id="4847f-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="4847f-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4847f-128">-IdentityType</span></span>
<span data-ttu-id="4847f-129">O tipo de identidade gerenciada usada.</span><span class="sxs-lookup"><span data-stu-id="4847f-129">The type of managed identity used.</span></span>
<span data-ttu-id="4847f-130">O tipo "SystemAssignedAndUserAssigned" inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4847f-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="4847f-131">O tipo "Nenhum" removerá qualquer identidade.</span><span class="sxs-lookup"><span data-stu-id="4847f-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="4847f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4847f-132">-InputObject</span></span>
<span data-ttu-id="4847f-133">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4847f-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4847f-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="4847f-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="4847f-135">A ID do cliente da identidade que será usada para acessar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4847f-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="4847f-136">-Name</span><span class="sxs-lookup"><span data-stu-id="4847f-136">-Name</span></span>
<span data-ttu-id="4847f-137">O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="4847f-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="4847f-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4847f-138">-NoWait</span></span>
<span data-ttu-id="4847f-139">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="4847f-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4847f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4847f-140">-ResourceGroupName</span></span>
<span data-ttu-id="4847f-141">O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="4847f-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="4847f-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="4847f-142">-Sku</span></span>
<span data-ttu-id="4847f-143">O nome SKU do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="4847f-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="4847f-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4847f-144">-SubscriptionId</span></span>
<span data-ttu-id="4847f-145">A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4847f-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="4847f-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="4847f-146">-Tag</span></span>
<span data-ttu-id="4847f-147">As ARM de recurso.</span><span class="sxs-lookup"><span data-stu-id="4847f-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="4847f-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4847f-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="4847f-149">A lista de identidades atribuídas pelo usuário associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="4847f-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="4847f-150">As chaves de dicionário de identidade atribuídas pelo usuário serão ARM ids de recurso no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="4847f-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="4847f-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4847f-151">-Confirm</span></span>
<span data-ttu-id="4847f-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4847f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4847f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4847f-153">-WhatIf</span></span>
<span data-ttu-id="4847f-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4847f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4847f-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4847f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4847f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4847f-156">CommonParameters</span></span>
<span data-ttu-id="4847f-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4847f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4847f-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4847f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4847f-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4847f-159">INPUTS</span></span>

### <span data-ttu-id="4847f-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="4847f-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="4847f-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4847f-161">OUTPUTS</span></span>

### <span data-ttu-id="4847f-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="4847f-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="4847f-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="4847f-163">NOTES</span></span>

<span data-ttu-id="4847f-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4847f-164">ALIASES</span></span>

<span data-ttu-id="4847f-165">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="4847f-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4847f-166">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4847f-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4847f-167">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4847f-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4847f-168">INPUTOBJECT <IAppConfigurationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="4847f-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4847f-169">`[ConfigStoreName <String>]`: O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="4847f-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="4847f-170">`[GroupName <String>]`: O nome do grupo de recursos de link privado.</span><span class="sxs-lookup"><span data-stu-id="4847f-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="4847f-171">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="4847f-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4847f-172">`[PrivateEndpointConnectionName <String>]`: Nome da conexão do ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="4847f-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="4847f-173">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="4847f-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="4847f-174">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4847f-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="4847f-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4847f-175">RELATED LINKS</span></span>



<span data-ttu-id="4847f-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="4847f-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

