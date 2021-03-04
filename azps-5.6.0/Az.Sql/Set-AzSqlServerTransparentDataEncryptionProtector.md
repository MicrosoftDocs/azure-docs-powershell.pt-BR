---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 992601b3a6d88c7aa424564189dc8af3efe6464d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887296"
---
# <span data-ttu-id="4808d-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4808d-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="4808d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4808d-102">SYNOPSIS</span></span>
<span data-ttu-id="4808d-103">Define o protetor TDE (Criptografia de Dados Transparentes) para um SQL servidor.</span><span class="sxs-lookup"><span data-stu-id="4808d-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="4808d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4808d-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4808d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4808d-105">DESCRIPTION</span></span>
<span data-ttu-id="4808d-106">O Set-AzSqlServerTransparentDataEncryptionProtector cmdlet define o protetor TDE para um SQL servidor.</span><span class="sxs-lookup"><span data-stu-id="4808d-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="4808d-107">Alterar o tipo de protetor TDE girará o protetor.</span><span class="sxs-lookup"><span data-stu-id="4808d-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="4808d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4808d-108">EXAMPLES</span></span>

### <span data-ttu-id="4808d-109">Exemplo 1: definir o tipo de protetor TDE (Criptografia de Dados Transparente) como ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="4808d-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="4808d-110">Este comando atualiza o tipo de protetor TDE de um servidor para Service Managed.</span><span class="sxs-lookup"><span data-stu-id="4808d-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="4808d-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="4808d-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="4808d-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="4808d-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="4808d-113">Exemplo 2: definir o tipo de protetor de Criptografia de Dados Transparente como Cofre de Chaves do Azure</span><span class="sxs-lookup"><span data-stu-id="4808d-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="4808d-114">Este comando atualiza um servidor para usar a Chave do Cofre de Chaves do Servidor com Id ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' como o protetor TDE.</span><span class="sxs-lookup"><span data-stu-id="4808d-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="4808d-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="4808d-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="4808d-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="4808d-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="4808d-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4808d-117">PARAMETERS</span></span>

### <span data-ttu-id="4808d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4808d-118">-AsJob</span></span>
<span data-ttu-id="4808d-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4808d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4808d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4808d-120">-DefaultProfile</span></span>
<span data-ttu-id="4808d-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4808d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4808d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4808d-122">-Force</span></span>
<span data-ttu-id="4808d-123">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="4808d-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4808d-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4808d-124">-KeyId</span></span>
<span data-ttu-id="4808d-125">KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4808d-125">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="4808d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4808d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4808d-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4808d-127">The name of the resource group</span></span>

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

### <span data-ttu-id="4808d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4808d-128">-ServerName</span></span>
<span data-ttu-id="4808d-129">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="4808d-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4808d-130">-Type</span><span class="sxs-lookup"><span data-stu-id="4808d-130">-Type</span></span>
<span data-ttu-id="4808d-131">O tipo de protetor TDE do Banco de Dados sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="4808d-131">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="4808d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4808d-132">-Confirm</span></span>
<span data-ttu-id="4808d-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4808d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4808d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4808d-134">-WhatIf</span></span>
<span data-ttu-id="4808d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4808d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4808d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4808d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4808d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4808d-137">CommonParameters</span></span>
<span data-ttu-id="4808d-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4808d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4808d-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4808d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4808d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4808d-140">INPUTS</span></span>

### <span data-ttu-id="4808d-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="4808d-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="4808d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4808d-142">System.String</span></span>

## <span data-ttu-id="4808d-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4808d-143">OUTPUTS</span></span>

### <span data-ttu-id="4808d-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="4808d-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="4808d-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="4808d-145">NOTES</span></span>

## <span data-ttu-id="4808d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4808d-146">RELATED LINKS</span></span>

[<span data-ttu-id="4808d-147">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="4808d-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
