---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280648"
---
# <span data-ttu-id="403dd-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="403dd-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="403dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="403dd-102">SYNOPSIS</span></span>
<span data-ttu-id="403dd-103">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="403dd-103">Updates a workspace.</span></span>

## <span data-ttu-id="403dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="403dd-104">SYNTAX</span></span>

### <span data-ttu-id="403dd-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="403dd-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="403dd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="403dd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="403dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="403dd-107">DESCRIPTION</span></span>
<span data-ttu-id="403dd-108">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="403dd-108">Updates a workspace.</span></span>

## <span data-ttu-id="403dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="403dd-109">EXAMPLES</span></span>

### <span data-ttu-id="403dd-110">Exemplo 1: atualiza as marcas de um espaço de trabalho databricks</span><span class="sxs-lookup"><span data-stu-id="403dd-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="403dd-111">Esse comando atualiza as marcas de um espaço de trabalho databricks.</span><span class="sxs-lookup"><span data-stu-id="403dd-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="403dd-112">Exemplo 2: habilitar a criptografia em um espaço de trabalho databricks</span><span class="sxs-lookup"><span data-stu-id="403dd-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="403dd-113">Habilitar a criptografia em um espaço de trabalho databricks usa três etapas:</span><span class="sxs-lookup"><span data-stu-id="403dd-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="403dd-114">Atualize o espaço de trabalho com `-PrepareEncryption` (se ele não tiver sido criado).</span><span class="sxs-lookup"><span data-stu-id="403dd-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="403dd-115">Localize `StorageAccountIdentityPrincipalId` na saída da última etapa.</span><span class="sxs-lookup"><span data-stu-id="403dd-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="403dd-116">Conceder permissões de chave para o principal.</span><span class="sxs-lookup"><span data-stu-id="403dd-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="403dd-117">Atualize o espaço de trabalho novamente para preencher as informações sobre a chave de criptografia:</span><span class="sxs-lookup"><span data-stu-id="403dd-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="403dd-118">Exemplo 3: desabilitar a criptografia em um espaço de trabalho databricks</span><span class="sxs-lookup"><span data-stu-id="403dd-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="403dd-119">Para desabilitar a criptografia, basta definir `-EncryptionKeySource` como `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="403dd-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="403dd-120">OS</span><span class="sxs-lookup"><span data-stu-id="403dd-120">PARAMETERS</span></span>

### <span data-ttu-id="403dd-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="403dd-121">-AsJob</span></span>
<span data-ttu-id="403dd-122">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="403dd-122">Run the command as a job</span></span>

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

### <span data-ttu-id="403dd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="403dd-123">-DefaultProfile</span></span>
<span data-ttu-id="403dd-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="403dd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="403dd-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="403dd-125">-EncryptionKeyName</span></span>
<span data-ttu-id="403dd-126">O nome da chave do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="403dd-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="403dd-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="403dd-127">-EncryptionKeySource</span></span>
<span data-ttu-id="403dd-128">A fonte de criptografia (provedor).</span><span class="sxs-lookup"><span data-stu-id="403dd-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="403dd-129">Valores possíveis (não diferencia maiúsculas de minúsculas): padrão, Microsoft. keyvault</span><span class="sxs-lookup"><span data-stu-id="403dd-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="403dd-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="403dd-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="403dd-131">O URI (nome DNS) do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="403dd-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="403dd-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="403dd-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="403dd-133">A versão da chave do keyvault.</span><span class="sxs-lookup"><span data-stu-id="403dd-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="403dd-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="403dd-134">-InputObject</span></span>
<span data-ttu-id="403dd-135">Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="403dd-135">Identity parameter.</span></span>
<span data-ttu-id="403dd-136">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="403dd-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="403dd-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="403dd-137">-Name</span></span>
<span data-ttu-id="403dd-138">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="403dd-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="403dd-139">-Nowait</span><span class="sxs-lookup"><span data-stu-id="403dd-139">-NoWait</span></span>
<span data-ttu-id="403dd-140">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="403dd-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="403dd-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="403dd-141">-PrepareEncryption</span></span>
<span data-ttu-id="403dd-142">Preparar o espaço de trabalho para criptografia.</span><span class="sxs-lookup"><span data-stu-id="403dd-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="403dd-143">Habilita a identidade gerenciada para a conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="403dd-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="403dd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="403dd-144">-ResourceGroupName</span></span>
<span data-ttu-id="403dd-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="403dd-145">The name of the resource group.</span></span>
<span data-ttu-id="403dd-146">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="403dd-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="403dd-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="403dd-147">-SubscriptionId</span></span>
<span data-ttu-id="403dd-148">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="403dd-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="403dd-149">-Marca</span><span class="sxs-lookup"><span data-stu-id="403dd-149">-Tag</span></span>
<span data-ttu-id="403dd-150">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="403dd-150">Resource tags.</span></span>

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

### <span data-ttu-id="403dd-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="403dd-151">-Confirm</span></span>
<span data-ttu-id="403dd-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="403dd-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="403dd-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="403dd-153">-WhatIf</span></span>
<span data-ttu-id="403dd-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="403dd-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="403dd-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="403dd-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="403dd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="403dd-156">CommonParameters</span></span>
<span data-ttu-id="403dd-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="403dd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="403dd-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="403dd-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="403dd-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="403dd-159">INPUTS</span></span>

### <span data-ttu-id="403dd-160">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="403dd-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="403dd-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="403dd-161">OUTPUTS</span></span>

### <span data-ttu-id="403dd-162">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="403dd-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="403dd-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="403dd-163">NOTES</span></span>

<span data-ttu-id="403dd-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="403dd-164">ALIASES</span></span>

<span data-ttu-id="403dd-165">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="403dd-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="403dd-166">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="403dd-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="403dd-167">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="403dd-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="403dd-168">INPUTobject <IDatabricksIdentity> : Parameter de identidade.</span><span class="sxs-lookup"><span data-stu-id="403dd-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="403dd-169">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="403dd-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="403dd-170">`[PeeringName <String>]`: O nome do emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="403dd-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="403dd-171">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="403dd-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="403dd-172">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="403dd-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="403dd-173">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="403dd-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="403dd-174">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="403dd-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="403dd-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="403dd-175">RELATED LINKS</span></span>

