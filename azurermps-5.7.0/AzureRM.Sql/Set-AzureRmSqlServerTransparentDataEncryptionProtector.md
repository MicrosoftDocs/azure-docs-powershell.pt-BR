---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: d78b6931e58469b20b2b937de083ff9d96f3f92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427407"
---
# <span data-ttu-id="f50f4-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f50f4-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="f50f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f50f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f50f4-103">Define o protetor de criptografia de dados transparente (TDE) para um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f50f4-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f50f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f50f4-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f50f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f50f4-105">DESCRIPTION</span></span>
<span data-ttu-id="f50f4-106">O cmdlet Set-AzureRmSqlServerTransparentDataEncryptionProtector define o protetor TDE para um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f50f4-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="f50f4-107">Alterar o tipo de protetor TDE irá rotacionar o protetor.</span><span class="sxs-lookup"><span data-stu-id="f50f4-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="f50f4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f50f4-108">EXAMPLES</span></span>

### <span data-ttu-id="f50f4-109">Exemplo 1: definir o tipo de protetor de criptografia de dados transparente (TDE) como não gerenciado</span><span class="sxs-lookup"><span data-stu-id="f50f4-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="f50f4-110">Esse comando atualiza o tipo de protetor do TDE do servidor para gerenciamento de serviço.</span><span class="sxs-lookup"><span data-stu-id="f50f4-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="f50f4-111">Tipo de ResourceGroupName nomedoservidor ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="f50f4-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="f50f4-112">ContosoResourceGroup ContosoServerd não gerenciado pela</span><span class="sxs-lookup"><span data-stu-id="f50f4-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="f50f4-113">Exemplo 2: definir o tipo de protetor de criptografia de dados transparente para o cofre de chaves do Azure</span><span class="sxs-lookup"><span data-stu-id="f50f4-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="f50f4-114">Este comando atualiza um servidor para usar a chave do cofre de chave do servidor com a ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' como o protetor TDE.</span><span class="sxs-lookup"><span data-stu-id="f50f4-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="f50f4-115">Tipo de ResourceGroupName nomedoservidor ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="f50f4-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="f50f4-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="f50f4-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="f50f4-117">OS</span><span class="sxs-lookup"><span data-stu-id="f50f4-117">PARAMETERS</span></span>

### <span data-ttu-id="f50f4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f50f4-118">-AsJob</span></span>
<span data-ttu-id="f50f4-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f50f4-119">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f50f4-120">-DefaultProfile</span></span>
<span data-ttu-id="f50f4-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f50f4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f50f4-122">-Force</span></span>
<span data-ttu-id="f50f4-123">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="f50f4-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f50f4-124">-KeyId</span></span>
<span data-ttu-id="f50f4-125">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f50f4-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f50f4-126">-ResourceGroupName</span></span>
<span data-ttu-id="f50f4-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f50f4-127">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f50f4-128">-ServerName</span></span>
<span data-ttu-id="f50f4-129">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="f50f4-129">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-130">-Digite</span><span class="sxs-lookup"><span data-stu-id="f50f4-130">-Type</span></span>
<span data-ttu-id="f50f4-131">O tipo de protetor do banco de dados SQL do Azure TDE.</span><span class="sxs-lookup"><span data-stu-id="f50f4-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f50f4-132">-Confirm</span></span>
<span data-ttu-id="f50f4-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f50f4-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f50f4-134">-WhatIf</span></span>
<span data-ttu-id="f50f4-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f50f4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f50f4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f50f4-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f50f4-137">CommonParameters</span></span>
<span data-ttu-id="f50f4-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f50f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f50f4-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f50f4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f50f4-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f50f4-140">INPUTS</span></span>

### <span data-ttu-id="f50f4-141">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="f50f4-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="f50f4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f50f4-142">System.String</span></span>

## <span data-ttu-id="f50f4-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f50f4-143">OUTPUTS</span></span>

### <span data-ttu-id="f50f4-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="f50f4-144">System.Object</span></span>

## <span data-ttu-id="f50f4-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f50f4-145">NOTES</span></span>

## <span data-ttu-id="f50f4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f50f4-146">RELATED LINKS</span></span>

[<span data-ttu-id="f50f4-147">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f50f4-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
