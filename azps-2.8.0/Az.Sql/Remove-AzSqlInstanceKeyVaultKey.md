---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 51b8af420ee619b3b07dfab8d03532c076312dc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773535"
---
# <span data-ttu-id="85051-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85051-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="85051-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85051-102">SYNOPSIS</span></span>
<span data-ttu-id="85051-103">Remove uma chave do cofre de chaves de uma instância gerenciada SQL</span><span class="sxs-lookup"><span data-stu-id="85051-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="85051-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85051-104">SYNTAX</span></span>

### <span data-ttu-id="85051-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="85051-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85051-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85051-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85051-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85051-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85051-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85051-108">DESCRIPTION</span></span>
<span data-ttu-id="85051-109">O cmdlet Remove-AzSqlInstanceKeyVaultKey remove a chave do cofre de chaves da instância gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="85051-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="85051-110">Observe que as permissões da instância gerenciada SQL para o cofre da chave não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="85051-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="85051-111">Para alterar permissões, use set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="85051-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="85051-112">Observe que esse cmdlet não faz alterações no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="85051-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="85051-113">Para remover uma chave do cofre de chaves, use remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="85051-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="85051-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85051-114">EXAMPLES</span></span>

### <span data-ttu-id="85051-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="85051-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="85051-116">Este comando Remove a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' da instância gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="85051-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="85051-117">Exemplo 2: usando o objeto de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="85051-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="85051-118">Este comando Remove a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' da instância gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="85051-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="85051-119">Exemplo 3: usando a ID do recurso de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="85051-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="85051-120">Este comando Remove a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' da instância gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="85051-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="85051-121">Exemplo 4: usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="85051-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="85051-122">Este comando Remove a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' da instância gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="85051-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="85051-123">OS</span><span class="sxs-lookup"><span data-stu-id="85051-123">PARAMETERS</span></span>

### <span data-ttu-id="85051-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85051-124">-DefaultProfile</span></span>
<span data-ttu-id="85051-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85051-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85051-126">-Instance</span><span class="sxs-lookup"><span data-stu-id="85051-126">-Instance</span></span>
<span data-ttu-id="85051-127">O objeto de entrada de instância</span><span class="sxs-lookup"><span data-stu-id="85051-127">The instance input object</span></span>

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

### <span data-ttu-id="85051-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="85051-128">-InstanceName</span></span>
<span data-ttu-id="85051-129">O nome da instância</span><span class="sxs-lookup"><span data-stu-id="85051-129">The instance name</span></span>

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

### <span data-ttu-id="85051-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="85051-130">-InstanceResourceId</span></span>
<span data-ttu-id="85051-131">A ID do recurso da instância</span><span class="sxs-lookup"><span data-stu-id="85051-131">The instance resource id</span></span>

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

### <span data-ttu-id="85051-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="85051-132">-KeyId</span></span>
<span data-ttu-id="85051-133">ID da chave AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="85051-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="85051-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85051-134">-ResourceGroupName</span></span>
<span data-ttu-id="85051-135">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="85051-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="85051-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85051-136">-Confirm</span></span>
<span data-ttu-id="85051-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85051-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85051-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85051-138">-WhatIf</span></span>
<span data-ttu-id="85051-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85051-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85051-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85051-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85051-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85051-141">CommonParameters</span></span>
<span data-ttu-id="85051-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85051-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85051-143">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85051-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85051-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85051-144">INPUTS</span></span>

### <span data-ttu-id="85051-145">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="85051-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="85051-146">System. String</span><span class="sxs-lookup"><span data-stu-id="85051-146">System.String</span></span>

## <span data-ttu-id="85051-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85051-147">OUTPUTS</span></span>

### <span data-ttu-id="85051-148">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="85051-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="85051-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85051-149">NOTES</span></span>

## <span data-ttu-id="85051-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85051-150">RELATED LINKS</span></span>