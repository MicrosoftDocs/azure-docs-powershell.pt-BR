---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112565"
---
# <span data-ttu-id="e583d-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e583d-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="e583d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e583d-102">SYNOPSIS</span></span>
<span data-ttu-id="e583d-103">Adiciona uma chave do cofre à Instância Gerenciada fornecida.</span><span class="sxs-lookup"><span data-stu-id="e583d-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="e583d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e583d-104">SYNTAX</span></span>

### <span data-ttu-id="e583d-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e583d-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e583d-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e583d-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e583d-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e583d-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e583d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e583d-108">DESCRIPTION</span></span>
<span data-ttu-id="e583d-109">O Add-AzSqlInstanceKeyVaultKey cmdlet adiciona uma chave do cofre à Instância Gerenciada fornecida.</span><span class="sxs-lookup"><span data-stu-id="e583d-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="e583d-110">A instância gerenciada deve ter permissões 'get, wrapKey, unwrapKey' para o cofre, use o seguinte script para conceder permissão à instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e583d-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="e583d-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwivaKey</span><span class="sxs-lookup"><span data-stu-id="e583d-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="e583d-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e583d-112">EXAMPLES</span></span>

### <span data-ttu-id="e583d-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e583d-113">Example 1</span></span>
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

<span data-ttu-id="e583d-114">Esse comando adiciona a chave do Cofre de Teclas com Id ' à instância gerenciada do SQL chamada https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoManagedInstanceName' no grupo de recursos 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="e583d-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="e583d-115">Exemplo 2: Usando objeto de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="e583d-115">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="e583d-116">Esse comando adiciona a chave do Cofre de Teclas com Id ' à instância gerenciada do SQL chamada https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoManagedInstanceName' no grupo de recursos 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="e583d-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="e583d-117">Exemplo 3: Usando a ID de recurso de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="e583d-117">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="e583d-118">Esse comando adiciona a chave do Cofre de Teclas com Id ' à instância gerenciada do SQL chamada https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoManagedInstanceName' no grupo de recursos 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="e583d-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="e583d-119">Exemplo 4: Usando a canalização</span><span class="sxs-lookup"><span data-stu-id="e583d-119">Example 4: Using piping</span></span>
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

<span data-ttu-id="e583d-120">Esse comando adiciona a chave do Cofre de Teclas com Id ' à instância gerenciada do SQL chamada https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoManagedInstanceName' no grupo de recursos 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="e583d-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="e583d-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e583d-121">PARAMETERS</span></span>

### <span data-ttu-id="e583d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e583d-122">-DefaultProfile</span></span>
<span data-ttu-id="e583d-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e583d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e583d-124">-Instância</span><span class="sxs-lookup"><span data-stu-id="e583d-124">-Instance</span></span>
<span data-ttu-id="e583d-125">O objeto de entrada de instância</span><span class="sxs-lookup"><span data-stu-id="e583d-125">The instance input object</span></span>

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

### <span data-ttu-id="e583d-126">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="e583d-126">-InstanceName</span></span>
<span data-ttu-id="e583d-127">O nome da instância</span><span class="sxs-lookup"><span data-stu-id="e583d-127">The instance name</span></span>

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

### <span data-ttu-id="e583d-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="e583d-128">-InstanceResourceId</span></span>
<span data-ttu-id="e583d-129">A ID do recurso de instância</span><span class="sxs-lookup"><span data-stu-id="e583d-129">The instance resource id</span></span>

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

### <span data-ttu-id="e583d-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e583d-130">-KeyId</span></span>
<span data-ttu-id="e583d-131">ID da chave do AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="e583d-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="e583d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e583d-132">-ResourceGroupName</span></span>
<span data-ttu-id="e583d-133">O Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e583d-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="e583d-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e583d-134">-Confirm</span></span>
<span data-ttu-id="e583d-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e583d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e583d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e583d-136">-WhatIf</span></span>
<span data-ttu-id="e583d-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e583d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e583d-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e583d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e583d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e583d-139">CommonParameters</span></span>
<span data-ttu-id="e583d-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e583d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e583d-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e583d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e583d-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="e583d-142">INPUTS</span></span>

### <span data-ttu-id="e583d-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e583d-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="e583d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e583d-144">System.String</span></span>

## <span data-ttu-id="e583d-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="e583d-145">OUTPUTS</span></span>

### <span data-ttu-id="e583d-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="e583d-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="e583d-147">Notas</span><span class="sxs-lookup"><span data-stu-id="e583d-147">NOTES</span></span>

## <span data-ttu-id="e583d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e583d-148">RELATED LINKS</span></span>
