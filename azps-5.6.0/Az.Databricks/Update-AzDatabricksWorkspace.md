---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 10a3a4d77cd6156bc2d6abe64a60773582ec50b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886659"
---
# <span data-ttu-id="e1d70-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="e1d70-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="e1d70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d70-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d70-103">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1d70-103">Updates a workspace.</span></span>

## <span data-ttu-id="e1d70-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e1d70-104">SYNTAX</span></span>

### <span data-ttu-id="e1d70-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e1d70-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e1d70-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e1d70-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e1d70-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e1d70-107">DESCRIPTION</span></span>
<span data-ttu-id="e1d70-108">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1d70-108">Updates a workspace.</span></span>

## <span data-ttu-id="e1d70-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1d70-109">EXAMPLES</span></span>

### <span data-ttu-id="e1d70-110">Exemplo 1: atualiza as marcas de um espaço de trabalho Databricks</span><span class="sxs-lookup"><span data-stu-id="e1d70-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="e1d70-111">Este comando atualiza as marcas de um espaço de trabalho Databricks.</span><span class="sxs-lookup"><span data-stu-id="e1d70-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="e1d70-112">Exemplo 2: Habilitar a criptografia em um espaço de trabalho Databricks</span><span class="sxs-lookup"><span data-stu-id="e1d70-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="e1d70-113">Habilenciar a criptografia em um espaço de trabalho Databricks leva três etapas:</span><span class="sxs-lookup"><span data-stu-id="e1d70-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="e1d70-114">Atualize o espaço de trabalho `-PrepareEncryption` com (se não foi criado assim).</span><span class="sxs-lookup"><span data-stu-id="e1d70-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="e1d70-115">Encontre `StorageAccountIdentityPrincipalId` na saída da última etapa.</span><span class="sxs-lookup"><span data-stu-id="e1d70-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="e1d70-116">Conceda permissões de chave à entidade principal.</span><span class="sxs-lookup"><span data-stu-id="e1d70-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="e1d70-117">Atualize o espaço de trabalho novamente para preencher informações sobre a chave de criptografia:</span><span class="sxs-lookup"><span data-stu-id="e1d70-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="e1d70-118">Exemplo 3: Desabilitar a criptografia em um espaço de trabalho Databricks</span><span class="sxs-lookup"><span data-stu-id="e1d70-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="e1d70-119">Para desabilitar a criptografia, basta definir `-EncryptionKeySource` como `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="e1d70-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="e1d70-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e1d70-120">PARAMETERS</span></span>

### <span data-ttu-id="e1d70-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1d70-121">-AsJob</span></span>
<span data-ttu-id="e1d70-122">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="e1d70-122">Run the command as a job</span></span>

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

### <span data-ttu-id="e1d70-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d70-123">-DefaultProfile</span></span>
<span data-ttu-id="e1d70-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d70-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1d70-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="e1d70-125">-EncryptionKeyName</span></span>
<span data-ttu-id="e1d70-126">O nome da chave do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="e1d70-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="e1d70-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="e1d70-127">-EncryptionKeySource</span></span>
<span data-ttu-id="e1d70-128">A chave de criptografiaSource (provedor).</span><span class="sxs-lookup"><span data-stu-id="e1d70-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="e1d70-129">Valores possíveis (sem maiúsculas de minúsculas): Padrão, Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="e1d70-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="e1d70-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e1d70-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="e1d70-131">O URI (nome DNS) do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="e1d70-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="e1d70-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e1d70-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="e1d70-133">A versão da tecla KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e1d70-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="e1d70-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1d70-134">-InputObject</span></span>
<span data-ttu-id="e1d70-135">Parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="e1d70-135">Identity parameter.</span></span>
<span data-ttu-id="e1d70-136">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e1d70-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e1d70-137">-Name</span><span class="sxs-lookup"><span data-stu-id="e1d70-137">-Name</span></span>
<span data-ttu-id="e1d70-138">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1d70-138">The name of the workspace.</span></span>

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

### <span data-ttu-id="e1d70-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e1d70-139">-NoWait</span></span>
<span data-ttu-id="e1d70-140">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="e1d70-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e1d70-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="e1d70-141">-PrepareEncryption</span></span>
<span data-ttu-id="e1d70-142">Preparar o espaço de trabalho para criptografia.</span><span class="sxs-lookup"><span data-stu-id="e1d70-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="e1d70-143">Habilita a Identidade Gerenciada para conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e1d70-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="e1d70-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d70-144">-ResourceGroupName</span></span>
<span data-ttu-id="e1d70-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1d70-145">The name of the resource group.</span></span>
<span data-ttu-id="e1d70-146">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e1d70-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e1d70-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1d70-147">-SubscriptionId</span></span>
<span data-ttu-id="e1d70-148">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e1d70-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e1d70-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1d70-149">-Tag</span></span>
<span data-ttu-id="e1d70-150">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="e1d70-150">Resource tags.</span></span>

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

### <span data-ttu-id="e1d70-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1d70-151">-Confirm</span></span>
<span data-ttu-id="e1d70-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1d70-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d70-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d70-153">-WhatIf</span></span>
<span data-ttu-id="e1d70-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1d70-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1d70-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1d70-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d70-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d70-156">CommonParameters</span></span>
<span data-ttu-id="e1d70-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d70-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d70-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1d70-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d70-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1d70-159">INPUTS</span></span>

### <span data-ttu-id="e1d70-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="e1d70-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e1d70-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e1d70-161">OUTPUTS</span></span>

### <span data-ttu-id="e1d70-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="e1d70-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="e1d70-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="e1d70-163">NOTES</span></span>

<span data-ttu-id="e1d70-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e1d70-164">ALIASES</span></span>

<span data-ttu-id="e1d70-165">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e1d70-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e1d70-166">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e1d70-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1d70-167">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1d70-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e1d70-168">INPUTOBJECT <IDatabricksIdentity> : Parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="e1d70-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="e1d70-169">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e1d70-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e1d70-170">`[PeeringName <String>]`: O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1d70-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e1d70-171">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1d70-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e1d70-172">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e1d70-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="e1d70-173">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e1d70-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e1d70-174">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1d70-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e1d70-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1d70-175">RELATED LINKS</span></span>

