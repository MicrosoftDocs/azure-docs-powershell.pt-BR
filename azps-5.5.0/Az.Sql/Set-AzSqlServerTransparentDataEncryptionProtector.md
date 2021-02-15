---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114464"
---
# <span data-ttu-id="8421f-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8421f-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="8421f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8421f-102">SYNOPSIS</span></span>
<span data-ttu-id="8421f-103">Define a criptografia de dados transparentes (TDE) para um servidor SQL.</span><span class="sxs-lookup"><span data-stu-id="8421f-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="8421f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8421f-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8421f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8421f-105">DESCRIPTION</span></span>
<span data-ttu-id="8421f-106">O Set-AzSqlServerTransparentDataEncryptionProtector cmdlet define o TDE para um servidor SQL.</span><span class="sxs-lookup"><span data-stu-id="8421f-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="8421f-107">Alterar o tipo de ressarção TDE girará a seta.</span><span class="sxs-lookup"><span data-stu-id="8421f-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="8421f-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8421f-108">EXAMPLES</span></span>

### <span data-ttu-id="8421f-109">Exemplo 1: Definir o tipo de criptografia de dados transparentes (TDE) como ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="8421f-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="8421f-110">Esse comando atualiza o tipo de TDE de um servidor para a Service Managed.</span><span class="sxs-lookup"><span data-stu-id="8421f-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="8421f-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="8421f-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="8421f-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="8421f-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="8421f-113">Exemplo 2: Definir o tipo de criptografia de dados transparentes para o Cofre de Chave do Azure</span><span class="sxs-lookup"><span data-stu-id="8421f-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="8421f-114">Este comando atualiza um servidor para usar a Chave do Cofre de Chave do Servidor com Id https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' como o TDE.</span><span class="sxs-lookup"><span data-stu-id="8421f-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="8421f-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="8421f-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="8421f-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="8421f-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="8421f-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8421f-117">PARAMETERS</span></span>

### <span data-ttu-id="8421f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8421f-118">-AsJob</span></span>
<span data-ttu-id="8421f-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8421f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8421f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8421f-120">-DefaultProfile</span></span>
<span data-ttu-id="8421f-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8421f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8421f-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8421f-122">-Force</span></span>
<span data-ttu-id="8421f-123">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="8421f-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="8421f-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="8421f-124">-KeyId</span></span>
<span data-ttu-id="8421f-125">A KeyId do Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="8421f-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8421f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8421f-126">-ResourceGroupName</span></span>
<span data-ttu-id="8421f-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8421f-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8421f-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8421f-128">-ServerName</span></span>
<span data-ttu-id="8421f-129">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="8421f-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8421f-130">-Tipo</span><span class="sxs-lookup"><span data-stu-id="8421f-130">-Type</span></span>
<span data-ttu-id="8421f-131">O tipo de banco de dados TDE do Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="8421f-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8421f-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8421f-132">-Confirm</span></span>
<span data-ttu-id="8421f-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8421f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8421f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8421f-134">-WhatIf</span></span>
<span data-ttu-id="8421f-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8421f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8421f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8421f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8421f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8421f-137">CommonParameters</span></span>
<span data-ttu-id="8421f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8421f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8421f-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8421f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8421f-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="8421f-140">INPUTS</span></span>

### <span data-ttu-id="8421f-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="8421f-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="8421f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8421f-142">System.String</span></span>

## <span data-ttu-id="8421f-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="8421f-143">OUTPUTS</span></span>

### <span data-ttu-id="8421f-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="8421f-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="8421f-145">Notas</span><span class="sxs-lookup"><span data-stu-id="8421f-145">NOTES</span></span>

## <span data-ttu-id="8421f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8421f-146">RELATED LINKS</span></span>

[<span data-ttu-id="8421f-147">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="8421f-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
