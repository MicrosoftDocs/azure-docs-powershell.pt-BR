---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116227"
---
# <span data-ttu-id="4de8d-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="4de8d-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="4de8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4de8d-102">SYNOPSIS</span></span>
<span data-ttu-id="4de8d-103">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4de8d-103">Updates a workspace.</span></span>

## <span data-ttu-id="4de8d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4de8d-104">SYNTAX</span></span>

### <span data-ttu-id="4de8d-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4de8d-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4de8d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4de8d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4de8d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4de8d-107">DESCRIPTION</span></span>
<span data-ttu-id="4de8d-108">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4de8d-108">Updates a workspace.</span></span>

## <span data-ttu-id="4de8d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4de8d-109">EXAMPLES</span></span>

### <span data-ttu-id="4de8d-110">Exemplo 1: atualiza as marcas de um espaço de trabalho Databções</span><span class="sxs-lookup"><span data-stu-id="4de8d-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="4de8d-111">Este comando atualiza as marcas de um espaço de trabalho Datab jerseys.</span><span class="sxs-lookup"><span data-stu-id="4de8d-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="4de8d-112">Exemplo 2: Habilitar a criptografia em um espaço de trabalho Datab bits</span><span class="sxs-lookup"><span data-stu-id="4de8d-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="4de8d-113">A habilitação da criptografia em um espaço de trabalho Datab bits requer três etapas:</span><span class="sxs-lookup"><span data-stu-id="4de8d-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="4de8d-114">Atualize o espaço de trabalho `-PrepareEncryption` com (se não tiver sido criado).</span><span class="sxs-lookup"><span data-stu-id="4de8d-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="4de8d-115">Encontre `StorageAccountIdentityPrincipalId` na saída da última etapa.</span><span class="sxs-lookup"><span data-stu-id="4de8d-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="4de8d-116">Conceda permissões de chave ao diretor.</span><span class="sxs-lookup"><span data-stu-id="4de8d-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="4de8d-117">Atualize o espaço de trabalho novamente para preencher informações sobre a chave de criptografia:</span><span class="sxs-lookup"><span data-stu-id="4de8d-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="4de8d-118">Exemplo 3: Desabilitar a criptografia em um espaço de trabalho Datab firewalls</span><span class="sxs-lookup"><span data-stu-id="4de8d-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="4de8d-119">Para desabilitar a criptografia, basta definir `-EncryptionKeySource` como `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="4de8d-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="4de8d-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4de8d-120">PARAMETERS</span></span>

### <span data-ttu-id="4de8d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4de8d-121">-AsJob</span></span>
<span data-ttu-id="4de8d-122">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="4de8d-122">Run the command as a job</span></span>

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

### <span data-ttu-id="4de8d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de8d-123">-DefaultProfile</span></span>
<span data-ttu-id="4de8d-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4de8d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de8d-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="4de8d-125">-EncryptionKeyName</span></span>
<span data-ttu-id="4de8d-126">O nome da chave do Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="4de8d-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="4de8d-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="4de8d-127">-EncryptionKeySource</span></span>
<span data-ttu-id="4de8d-128">A chave de criptografiaSource (provedor).</span><span class="sxs-lookup"><span data-stu-id="4de8d-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="4de8d-129">Valores possíveis (sem maiúsculas de minúsculas): Default, Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="4de8d-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="4de8d-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="4de8d-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="4de8d-131">O URI (nome DNS) do Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="4de8d-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="4de8d-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="4de8d-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="4de8d-133">A versão da tecla KeyVault.</span><span class="sxs-lookup"><span data-stu-id="4de8d-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="4de8d-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4de8d-134">-InputObject</span></span>
<span data-ttu-id="4de8d-135">Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="4de8d-135">Identity parameter.</span></span>
<span data-ttu-id="4de8d-136">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4de8d-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4de8d-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="4de8d-137">-Name</span></span>
<span data-ttu-id="4de8d-138">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4de8d-138">The name of the workspace.</span></span>

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

### <span data-ttu-id="4de8d-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4de8d-139">-NoWait</span></span>
<span data-ttu-id="4de8d-140">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="4de8d-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4de8d-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="4de8d-141">-PrepareEncryption</span></span>
<span data-ttu-id="4de8d-142">Preparar o espaço de trabalho para criptografia.</span><span class="sxs-lookup"><span data-stu-id="4de8d-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="4de8d-143">Habilita a Identidade Gerenciada para a conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4de8d-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="4de8d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de8d-144">-ResourceGroupName</span></span>
<span data-ttu-id="4de8d-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4de8d-145">The name of the resource group.</span></span>
<span data-ttu-id="4de8d-146">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4de8d-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4de8d-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4de8d-147">-SubscriptionId</span></span>
<span data-ttu-id="4de8d-148">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4de8d-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4de8d-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="4de8d-149">-Tag</span></span>
<span data-ttu-id="4de8d-150">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="4de8d-150">Resource tags.</span></span>

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

### <span data-ttu-id="4de8d-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4de8d-151">-Confirm</span></span>
<span data-ttu-id="4de8d-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4de8d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de8d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de8d-153">-WhatIf</span></span>
<span data-ttu-id="4de8d-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4de8d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4de8d-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4de8d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de8d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de8d-156">CommonParameters</span></span>
<span data-ttu-id="4de8d-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de8d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de8d-158">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4de8d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de8d-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="4de8d-159">INPUTS</span></span>

### <span data-ttu-id="4de8d-160">Microsoft.Azure.PowerShell.Cmdlets.Databndezs.Models.IDatabtabçõesIdentity</span><span class="sxs-lookup"><span data-stu-id="4de8d-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="4de8d-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="4de8d-161">OUTPUTS</span></span>

### <span data-ttu-id="4de8d-162">Microsoft.Azure.PowerShell.Cmdlets.Datab sérvios.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="4de8d-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="4de8d-163">Notas</span><span class="sxs-lookup"><span data-stu-id="4de8d-163">NOTES</span></span>

<span data-ttu-id="4de8d-164">Aliases</span><span class="sxs-lookup"><span data-stu-id="4de8d-164">ALIASES</span></span>

<span data-ttu-id="4de8d-165">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4de8d-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4de8d-166">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4de8d-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4de8d-167">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4de8d-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4de8d-168">INPUTOBJECT: <IDatabricksIdentity> Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="4de8d-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="4de8d-169">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4de8d-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4de8d-170">`[PeeringName <String>]`: o nome do pario vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4de8d-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="4de8d-171">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4de8d-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4de8d-172">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4de8d-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="4de8d-173">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4de8d-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4de8d-174">`[WorkspaceName <String>]`: o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4de8d-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="4de8d-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4de8d-175">RELATED LINKS</span></span>

