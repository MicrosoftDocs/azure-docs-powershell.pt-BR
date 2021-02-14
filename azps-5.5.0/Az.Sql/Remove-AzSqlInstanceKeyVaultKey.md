---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110922"
---
# <span data-ttu-id="8f5c2-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8f5c2-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="8f5c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5c2-103">Remove uma chave do Cofre de Teclas de uma instância gerenciada pelo SQL</span><span class="sxs-lookup"><span data-stu-id="8f5c2-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="8f5c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f5c2-104">SYNTAX</span></span>

### <span data-ttu-id="8f5c2-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f5c2-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f5c2-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f5c2-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f5c2-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f5c2-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f5c2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f5c2-108">DESCRIPTION</span></span>
<span data-ttu-id="8f5c2-109">O Remove-AzSqlInstanceKeyVaultKey cmdlet remove a tecla Key Vault da Instância Gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="8f5c2-110">Observe que as permissões da instância gerenciada pelo SQL para o cofre da chave não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="8f5c2-111">Para alterar as permissões, use Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="8f5c2-112">Observe que esse cmdlet não faz alterações no Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="8f5c2-113">Para remover uma chave do Cofre de Teclas, use Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="8f5c2-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f5c2-114">EXAMPLES</span></span>

### <span data-ttu-id="8f5c2-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f5c2-115">Example 1</span></span>
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

<span data-ttu-id="8f5c2-116">Esse comando remove a tecla Key Vault com Id ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 da instância gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="8f5c2-117">Exemplo 2: Usando objeto de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="8f5c2-117">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="8f5c2-118">Esse comando remove a tecla Key Vault com Id ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 da instância gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="8f5c2-119">Exemplo 3: Usando a ID de recurso de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="8f5c2-119">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="8f5c2-120">Esse comando remove a tecla Key Vault com Id ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 da instância gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="8f5c2-121">Exemplo 4: Usando a canalização</span><span class="sxs-lookup"><span data-stu-id="8f5c2-121">Example 4: Using piping</span></span>
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

<span data-ttu-id="8f5c2-122">Esse comando remove a tecla Key Vault com Id ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 da instância gerenciada especificada.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="8f5c2-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f5c2-123">PARAMETERS</span></span>

### <span data-ttu-id="8f5c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5c2-124">-DefaultProfile</span></span>
<span data-ttu-id="8f5c2-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f5c2-126">-Instância</span><span class="sxs-lookup"><span data-stu-id="8f5c2-126">-Instance</span></span>
<span data-ttu-id="8f5c2-127">O objeto de entrada de instância</span><span class="sxs-lookup"><span data-stu-id="8f5c2-127">The instance input object</span></span>

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

### <span data-ttu-id="8f5c2-128">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="8f5c2-128">-InstanceName</span></span>
<span data-ttu-id="8f5c2-129">O nome da instância</span><span class="sxs-lookup"><span data-stu-id="8f5c2-129">The instance name</span></span>

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

### <span data-ttu-id="8f5c2-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="8f5c2-130">-InstanceResourceId</span></span>
<span data-ttu-id="8f5c2-131">A ID do recurso de instância</span><span class="sxs-lookup"><span data-stu-id="8f5c2-131">The instance resource id</span></span>

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

### <span data-ttu-id="8f5c2-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="8f5c2-132">-KeyId</span></span>
<span data-ttu-id="8f5c2-133">ID da chave do AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="8f5c2-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="8f5c2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f5c2-134">-ResourceGroupName</span></span>
<span data-ttu-id="8f5c2-135">O Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8f5c2-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="8f5c2-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8f5c2-136">-Confirm</span></span>
<span data-ttu-id="8f5c2-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f5c2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f5c2-138">-WhatIf</span></span>
<span data-ttu-id="8f5c2-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f5c2-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f5c2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5c2-141">CommonParameters</span></span>
<span data-ttu-id="8f5c2-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f5c2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5c2-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f5c2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5c2-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f5c2-144">INPUTS</span></span>

### <span data-ttu-id="8f5c2-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8f5c2-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="8f5c2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="8f5c2-146">System.String</span></span>

## <span data-ttu-id="8f5c2-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f5c2-147">OUTPUTS</span></span>

### <span data-ttu-id="8f5c2-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="8f5c2-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="8f5c2-149">Notas</span><span class="sxs-lookup"><span data-stu-id="8f5c2-149">NOTES</span></span>

## <span data-ttu-id="8f5c2-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f5c2-150">RELATED LINKS</span></span>
