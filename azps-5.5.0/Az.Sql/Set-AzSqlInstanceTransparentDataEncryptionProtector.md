---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115701"
---
# <span data-ttu-id="c1a0f-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c1a0f-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="c1a0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a0f-103">Define a criptografia de dados transparente (TDE) para uma instância gerenciada pelo SQL.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="c1a0f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1a0f-104">SYNTAX</span></span>

### <span data-ttu-id="c1a0f-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c1a0f-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a0f-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1a0f-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a0f-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1a0f-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1a0f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1a0f-108">DESCRIPTION</span></span>
<span data-ttu-id="c1a0f-109">O Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet define o formato TDE para uma instância gerenciada pelo SQL.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="c1a0f-110">Alterar o tipo de ressarção TDE girará a seta.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="c1a0f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1a0f-111">EXAMPLES</span></span>

### <span data-ttu-id="c1a0f-112">Exemplo 1: Definir o tipo de criptografia de dados transparentes (TDE) como ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="c1a0f-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="c1a0f-113">Esse comando atualiza o tipo de TDE de uma instância gerenciada para a Service Managed.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="c1a0f-114">Exemplo 2: Definir o tipo de criptografia de dados transparentes para o Cofre de Chave do Azure</span><span class="sxs-lookup"><span data-stu-id="c1a0f-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c1a0f-115">Esse comando atualiza a instância gerenciada especificada para usar a Chave do Cofre de Chave de Instância Gerenciada com Id ' como o https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 comando TDE.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="c1a0f-116">Exemplo 3: Definir o tipo de criptografia de dados transparentes para o Cofre de Chave do Azure usando o objeto de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="c1a0f-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c1a0f-117">Esse comando atualiza a instância gerenciada especificada para usar a Chave do Cofre de Chave de Instância Gerenciada com Id ' como o https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 comando TDE.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="c1a0f-118">Exemplo 4: Definir o tipo de criptografia de dados transparentes para o Cofre de Chave do Azure usando a ID do recurso</span><span class="sxs-lookup"><span data-stu-id="c1a0f-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c1a0f-119">Esse comando atualiza a instância gerenciada especificada para usar a Chave do Cofre de Chave de Instância Gerenciada com Id ' como o https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 comando TDE.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="c1a0f-120">Exemplo 5: Definir o tipo de criptografia de dados transparentes para o Cofre de Chave do Azure usando a piping</span><span class="sxs-lookup"><span data-stu-id="c1a0f-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c1a0f-121">Esse comando atualiza a instância gerenciada especificada para usar a Chave do Cofre de Chave de Instância Gerenciada com Id ' como o https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 comando TDE.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="c1a0f-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1a0f-122">PARAMETERS</span></span>

### <span data-ttu-id="c1a0f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a0f-123">-DefaultProfile</span></span>
<span data-ttu-id="c1a0f-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1a0f-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c1a0f-125">-Force</span></span>
<span data-ttu-id="c1a0f-126">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="c1a0f-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c1a0f-127">-Instância</span><span class="sxs-lookup"><span data-stu-id="c1a0f-127">-Instance</span></span>
<span data-ttu-id="c1a0f-128">O objeto de entrada de instância</span><span class="sxs-lookup"><span data-stu-id="c1a0f-128">The instance input object</span></span>

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

### <span data-ttu-id="c1a0f-129">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="c1a0f-129">-InstanceName</span></span>
<span data-ttu-id="c1a0f-130">O nome da instância</span><span class="sxs-lookup"><span data-stu-id="c1a0f-130">The instance name</span></span>

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

### <span data-ttu-id="c1a0f-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="c1a0f-131">-InstanceResourceId</span></span>
<span data-ttu-id="c1a0f-132">A ID do recurso de instância</span><span class="sxs-lookup"><span data-stu-id="c1a0f-132">The instance resource id</span></span>

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

### <span data-ttu-id="c1a0f-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c1a0f-133">-KeyId</span></span>
<span data-ttu-id="c1a0f-134">A KeyId do Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="c1a0f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a0f-135">-ResourceGroupName</span></span>
<span data-ttu-id="c1a0f-136">O Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c1a0f-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="c1a0f-137">-Tipo</span><span class="sxs-lookup"><span data-stu-id="c1a0f-137">-Type</span></span>
<span data-ttu-id="c1a0f-138">O tipo de criptografia de criptografia de dados transparente do banco de dados sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="c1a0f-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c1a0f-139">-Confirm</span></span>
<span data-ttu-id="c1a0f-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1a0f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1a0f-141">-WhatIf</span></span>
<span data-ttu-id="c1a0f-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1a0f-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1a0f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a0f-144">CommonParameters</span></span>
<span data-ttu-id="c1a0f-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a0f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a0f-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1a0f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a0f-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="c1a0f-147">INPUTS</span></span>

### <span data-ttu-id="c1a0f-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c1a0f-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="c1a0f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c1a0f-149">System.String</span></span>

## <span data-ttu-id="c1a0f-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="c1a0f-150">OUTPUTS</span></span>

### <span data-ttu-id="c1a0f-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="c1a0f-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="c1a0f-152">Notas</span><span class="sxs-lookup"><span data-stu-id="c1a0f-152">NOTES</span></span>

## <span data-ttu-id="c1a0f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1a0f-153">RELATED LINKS</span></span>
