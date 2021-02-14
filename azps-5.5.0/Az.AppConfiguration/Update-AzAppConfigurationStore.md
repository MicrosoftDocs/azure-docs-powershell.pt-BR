---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 8aea57e0c2bea5dbaa2e3233e886c97bfebe4bd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115547"
---
# <span data-ttu-id="6907d-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="6907d-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="6907d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6907d-102">SYNOPSIS</span></span>
<span data-ttu-id="6907d-103">Atualiza um armazenamento de configurações com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="6907d-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="6907d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6907d-104">SYNTAX</span></span>

### <span data-ttu-id="6907d-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6907d-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6907d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6907d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6907d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6907d-107">DESCRIPTION</span></span>
<span data-ttu-id="6907d-108">Atualiza um armazenamento de configurações com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="6907d-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="6907d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6907d-109">EXAMPLES</span></span>

### <span data-ttu-id="6907d-110">Exemplo 1: Habilitar a criptografia de dados do armazenamento de configuração do aplicativo por identidade gerenciada atribuída pelo sistema</span><span class="sxs-lookup"><span data-stu-id="6907d-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6907d-111">Esse comando habilita a criptografia de dados por uma chave armazenada no Cofre de Teclas do Azure usando uma identidade gerenciada atribuída pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6907d-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="6907d-112">O cofre deve ter habilitado a exclusão suave e a proteção contra limpeza, e a identidade gerenciada deve ter essas permissões principais: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="6907d-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="6907d-113">Exemplo 2: Habilitar a criptografia de dados do armazenamento de configuração do aplicativo por identidade gerenciada atribuída pelo usuário</span><span class="sxs-lookup"><span data-stu-id="6907d-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="6907d-114">Esse comando habilita a criptografia de dados por uma chave armazenada no Cofre de Teclas do Azure usando uma identidade gerenciada atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6907d-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="6907d-115">A identidade atribuída pelo usuário deve ter sido definida com `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="6907d-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="6907d-116">O cofre deve ter habilitado a exclusão suave e a proteção contra limpeza, e a identidade gerenciada deve ter essas permissões principais: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="6907d-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="6907d-117">Exemplo 3: Desabilitar a criptografia de um armazenamento de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6907d-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6907d-118">Esse comando desabilita a criptografia de um armazenamento de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6907d-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="6907d-119">Exemplo 3: Atualizar sku e marca de um armazenamento de configuração de aplicativo por pipeline.</span><span class="sxs-lookup"><span data-stu-id="6907d-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="6907d-120">Este comando atualiza a SKU e a marca de um armazenamento de configuração de aplicativo por pipeline.</span><span class="sxs-lookup"><span data-stu-id="6907d-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="6907d-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6907d-121">PARAMETERS</span></span>

### <span data-ttu-id="6907d-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6907d-122">-AsJob</span></span>
<span data-ttu-id="6907d-123">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6907d-123">Run the command as a job</span></span>

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

### <span data-ttu-id="6907d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6907d-124">-DefaultProfile</span></span>
<span data-ttu-id="6907d-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6907d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6907d-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="6907d-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="6907d-127">O URI da chave do cofre de chave usada para criptografar dados.</span><span class="sxs-lookup"><span data-stu-id="6907d-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="6907d-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6907d-128">-IdentityType</span></span>
<span data-ttu-id="6907d-129">O tipo de identidade gerenciada usada.</span><span class="sxs-lookup"><span data-stu-id="6907d-129">The type of managed identity used.</span></span>
<span data-ttu-id="6907d-130">O tipo "SystemAssignedAndUserAssigned" inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6907d-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="6907d-131">O tipo "Nenhum" removerá as identidades.</span><span class="sxs-lookup"><span data-stu-id="6907d-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="6907d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6907d-132">-InputObject</span></span>
<span data-ttu-id="6907d-133">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="6907d-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6907d-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="6907d-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="6907d-135">A ID do cliente da identidade que será usada para acessar o cofre de teclas.</span><span class="sxs-lookup"><span data-stu-id="6907d-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="6907d-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="6907d-136">-Name</span></span>
<span data-ttu-id="6907d-137">O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="6907d-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="6907d-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6907d-138">-NoWait</span></span>
<span data-ttu-id="6907d-139">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="6907d-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6907d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6907d-140">-ResourceGroupName</span></span>
<span data-ttu-id="6907d-141">O nome do grupo de recursos ao qual o registro de contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="6907d-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="6907d-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="6907d-142">-Sku</span></span>
<span data-ttu-id="6907d-143">O nome SKU do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="6907d-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="6907d-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6907d-144">-SubscriptionId</span></span>
<span data-ttu-id="6907d-145">A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6907d-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="6907d-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="6907d-146">-Tag</span></span>
<span data-ttu-id="6907d-147">As marcas de recurso ARM.</span><span class="sxs-lookup"><span data-stu-id="6907d-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="6907d-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6907d-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="6907d-149">A lista de identidades atribuídas pelo usuário associada ao recurso.</span><span class="sxs-lookup"><span data-stu-id="6907d-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="6907d-150">As chaves do dicionário de identidade atribuídas pelo usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="6907d-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="6907d-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6907d-151">-Confirm</span></span>
<span data-ttu-id="6907d-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6907d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6907d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6907d-153">-WhatIf</span></span>
<span data-ttu-id="6907d-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6907d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6907d-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6907d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6907d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6907d-156">CommonParameters</span></span>
<span data-ttu-id="6907d-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6907d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6907d-158">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6907d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6907d-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="6907d-159">INPUTS</span></span>

### <span data-ttu-id="6907d-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="6907d-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="6907d-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="6907d-161">OUTPUTS</span></span>

### <span data-ttu-id="6907d-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="6907d-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="6907d-163">Notas</span><span class="sxs-lookup"><span data-stu-id="6907d-163">NOTES</span></span>

<span data-ttu-id="6907d-164">Aliases</span><span class="sxs-lookup"><span data-stu-id="6907d-164">ALIASES</span></span>

<span data-ttu-id="6907d-165">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="6907d-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6907d-166">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6907d-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6907d-167">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6907d-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6907d-168">INPUTOBJECT: <IAppConfigurationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="6907d-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6907d-169">`[ConfigStoreName <String>]`: o nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="6907d-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="6907d-170">`[GroupName <String>]`: o nome do grupo de recursos de vínculo privado.</span><span class="sxs-lookup"><span data-stu-id="6907d-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="6907d-171">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="6907d-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6907d-172">`[PrivateEndpointConnectionName <String>]`: Nome de conexão do ponto de extremidade particular</span><span class="sxs-lookup"><span data-stu-id="6907d-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="6907d-173">`[ResourceGroupName <String>]`: o nome do grupo de recursos ao qual o registro de contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="6907d-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="6907d-174">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6907d-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="6907d-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6907d-175">RELATED LINKS</span></span>



<span data-ttu-id="6907d-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="6907d-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

