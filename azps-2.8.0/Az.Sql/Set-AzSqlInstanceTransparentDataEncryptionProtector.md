---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 0321fc68c22e3bea973c25f9bbb27e0c5736e944
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773700"
---
# <span data-ttu-id="c541a-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c541a-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="c541a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c541a-102">SYNOPSIS</span></span>
<span data-ttu-id="c541a-103">Define o protetor de criptografia de dados transparente (TDE) para uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="c541a-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="c541a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c541a-104">SYNTAX</span></span>

### <span data-ttu-id="c541a-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c541a-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c541a-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c541a-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c541a-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c541a-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c541a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c541a-108">DESCRIPTION</span></span>
<span data-ttu-id="c541a-109">O cmdlet Set-AzSqlInstanceTransparentDataEncryptionProtector define o protetor TDE para uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="c541a-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="c541a-110">Alterar o tipo de protetor TDE irá rotacionar o protetor.</span><span class="sxs-lookup"><span data-stu-id="c541a-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="c541a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c541a-111">EXAMPLES</span></span>

### <span data-ttu-id="c541a-112">Exemplo 1: definir o tipo de protetor de criptografia de dados transparente (TDE) como não gerenciado</span><span class="sxs-lookup"><span data-stu-id="c541a-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="c541a-113">Esse comando atualiza o tipo de protetor TDE de uma instância gerenciada para o serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c541a-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="c541a-114">Exemplo 2: definir o tipo de protetor de criptografia de dados transparente para o cofre de chaves do Azure</span><span class="sxs-lookup"><span data-stu-id="c541a-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c541a-115">Esse comando atualiza a instância gerenciada especificada para usar a chave do cofre da chave de instância gerenciada com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' como o protetor TDE.</span><span class="sxs-lookup"><span data-stu-id="c541a-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="c541a-116">Exemplo 3: definir o tipo de protetor de criptografia de dados transparente para o cofre de chaves do Azure usando o objeto de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="c541a-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c541a-117">Esse comando atualiza a instância gerenciada especificada para usar a chave do cofre da chave de instância gerenciada com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' como o protetor TDE.</span><span class="sxs-lookup"><span data-stu-id="c541a-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="c541a-118">Exemplo 4: definir o tipo de protetor de criptografia de dados transparente para o cofre de chaves do Azure usando a ID do recurso</span><span class="sxs-lookup"><span data-stu-id="c541a-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c541a-119">Esse comando atualiza a instância gerenciada especificada para usar a chave do cofre da chave de instância gerenciada com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' como o protetor TDE.</span><span class="sxs-lookup"><span data-stu-id="c541a-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="c541a-120">Exemplo 5: definir o tipo de protetor de criptografia de dados transparente para o cofre de chaves do Azure usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="c541a-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c541a-121">Esse comando atualiza a instância gerenciada especificada para usar a chave do cofre da chave de instância gerenciada com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' como o protetor TDE.</span><span class="sxs-lookup"><span data-stu-id="c541a-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="c541a-122">OS</span><span class="sxs-lookup"><span data-stu-id="c541a-122">PARAMETERS</span></span>

### <span data-ttu-id="c541a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c541a-123">-DefaultProfile</span></span>
<span data-ttu-id="c541a-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c541a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c541a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c541a-125">-Force</span></span>
<span data-ttu-id="c541a-126">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="c541a-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c541a-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="c541a-127">-Instance</span></span>
<span data-ttu-id="c541a-128">O objeto de entrada de instância</span><span class="sxs-lookup"><span data-stu-id="c541a-128">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c541a-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c541a-129">-InstanceName</span></span>
<span data-ttu-id="c541a-130">O nome da instância</span><span class="sxs-lookup"><span data-stu-id="c541a-130">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541a-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="c541a-131">-InstanceResourceId</span></span>
<span data-ttu-id="c541a-132">A ID do recurso da instância</span><span class="sxs-lookup"><span data-stu-id="c541a-132">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c541a-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c541a-133">-KeyId</span></span>
<span data-ttu-id="c541a-134">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c541a-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c541a-135">-ResourceGroupName</span></span>
<span data-ttu-id="c541a-136">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c541a-136">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541a-137">-Digite</span><span class="sxs-lookup"><span data-stu-id="c541a-137">-Type</span></span>
<span data-ttu-id="c541a-138">O tipo de protetor de criptografia de dados transparente do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c541a-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c541a-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c541a-139">-Confirm</span></span>
<span data-ttu-id="c541a-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c541a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c541a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c541a-141">-WhatIf</span></span>
<span data-ttu-id="c541a-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c541a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c541a-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c541a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c541a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c541a-144">CommonParameters</span></span>
<span data-ttu-id="c541a-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c541a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c541a-146">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c541a-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c541a-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c541a-147">INPUTS</span></span>

### <span data-ttu-id="c541a-148">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c541a-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="c541a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c541a-149">System.String</span></span>

## <span data-ttu-id="c541a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c541a-150">OUTPUTS</span></span>

### <span data-ttu-id="c541a-151">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="c541a-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="c541a-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c541a-152">NOTES</span></span>

## <span data-ttu-id="c541a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c541a-153">RELATED LINKS</span></span>
