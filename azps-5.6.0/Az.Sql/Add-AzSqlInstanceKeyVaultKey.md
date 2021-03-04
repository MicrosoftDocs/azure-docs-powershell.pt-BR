---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 5a83d442f0b12731de3a00468283a8539b529fa7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886576"
---
# <span data-ttu-id="e70aa-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e70aa-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="e70aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e70aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e70aa-103">Adiciona uma chave de cofre à Instância Gerenciada fornecida.</span><span class="sxs-lookup"><span data-stu-id="e70aa-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="e70aa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e70aa-104">SYNTAX</span></span>

### <span data-ttu-id="e70aa-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e70aa-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70aa-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e70aa-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70aa-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e70aa-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e70aa-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e70aa-108">DESCRIPTION</span></span>
<span data-ttu-id="e70aa-109">O Add-AzSqlInstanceKeyVaultKey cmdlet adiciona uma chave de cofre à Instância Gerenciada fornecida.</span><span class="sxs-lookup"><span data-stu-id="e70aa-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="e70aa-110">A instância gerenciada deve ter permissões 'get, wrapKey, unwrapKey' para o cofre, use o script a seguir para conceder permissão à instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e70aa-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="e70aa-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="e70aa-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="e70aa-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e70aa-112">EXAMPLES</span></span>

### <span data-ttu-id="e70aa-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e70aa-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="e70aa-114">Este comando adiciona a chave key vault com Id ' ' à instância gerenciada SQL https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 chamada 'ContosoManagedInstanceName' no grupo de recursos 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="e70aa-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="e70aa-115">Exemplo 2: Usando o objeto de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="e70aa-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="e70aa-116">Este comando adiciona a chave key vault com Id ' ' à instância gerenciada SQL https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 chamada 'ContosoManagedInstanceName' no grupo de recursos 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="e70aa-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="e70aa-117">Exemplo 3: Usando a ID de recurso de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="e70aa-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="e70aa-118">Este comando adiciona a chave key vault com Id ' ' à instância gerenciada SQL https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 chamada 'ContosoManagedInstanceName' no grupo de recursos 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="e70aa-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="e70aa-119">Exemplo 4: usando a canalização</span><span class="sxs-lookup"><span data-stu-id="e70aa-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="e70aa-120">Este comando adiciona a chave key vault com Id ' ' à instância gerenciada SQL https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 chamada 'ContosoManagedInstanceName' no grupo de recursos 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="e70aa-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="e70aa-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e70aa-121">PARAMETERS</span></span>

### <span data-ttu-id="e70aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70aa-122">-DefaultProfile</span></span>
<span data-ttu-id="e70aa-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e70aa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70aa-124">-Instance</span><span class="sxs-lookup"><span data-stu-id="e70aa-124">-Instance</span></span>
<span data-ttu-id="e70aa-125">O objeto de entrada de instância</span><span class="sxs-lookup"><span data-stu-id="e70aa-125">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e70aa-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e70aa-126">-InstanceName</span></span>
<span data-ttu-id="e70aa-127">O nome da instância</span><span class="sxs-lookup"><span data-stu-id="e70aa-127">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70aa-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="e70aa-128">-InstanceResourceId</span></span>
<span data-ttu-id="e70aa-129">A ID do recurso de instância</span><span class="sxs-lookup"><span data-stu-id="e70aa-129">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e70aa-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e70aa-130">-KeyId</span></span>
<span data-ttu-id="e70aa-131">ID da chave do AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="e70aa-131">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70aa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e70aa-132">-ResourceGroupName</span></span>
<span data-ttu-id="e70aa-133">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e70aa-133">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e70aa-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e70aa-134">-Confirm</span></span>
<span data-ttu-id="e70aa-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e70aa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e70aa-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e70aa-136">-WhatIf</span></span>
<span data-ttu-id="e70aa-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e70aa-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e70aa-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e70aa-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e70aa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70aa-139">CommonParameters</span></span>
<span data-ttu-id="e70aa-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e70aa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70aa-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e70aa-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70aa-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e70aa-142">INPUTS</span></span>

### <span data-ttu-id="e70aa-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e70aa-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="e70aa-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e70aa-144">System.String</span></span>

## <span data-ttu-id="e70aa-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e70aa-145">OUTPUTS</span></span>

### <span data-ttu-id="e70aa-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="e70aa-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="e70aa-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="e70aa-147">NOTES</span></span>

## <span data-ttu-id="e70aa-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e70aa-148">RELATED LINKS</span></span>
