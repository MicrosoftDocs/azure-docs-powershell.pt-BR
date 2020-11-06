---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 81ec18dd543a63a971d01a64c878774b266cf0fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440717"
---
# <span data-ttu-id="5cc2e-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5cc2e-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="5cc2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5cc2e-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc2e-103">Remove uma chave do cofre de chaves de um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cc2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cc2e-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cc2e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5cc2e-105">DESCRIPTION</span></span>
<span data-ttu-id="5cc2e-106">O cmdlet Remove-AzureRmSqlServerKeyVaultKey remove a chave do cofre de chaves do SQL Server especificado.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="5cc2e-107">Observe que as permissões do SQL Server para o cofre da chave não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="5cc2e-108">Para alterar permissões, use set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="5cc2e-109">Observe que esse cmdlet não faz alterações no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="5cc2e-110">Para remover uma chave do cofre de chaves, use remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="5cc2e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5cc2e-111">EXAMPLES</span></span>

### <span data-ttu-id="5cc2e-112">Exemplo 1: remover uma chave do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="5cc2e-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="5cc2e-113">Este comando Remove a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="5cc2e-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="5cc2e-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="5cc2e-115">OS</span><span class="sxs-lookup"><span data-stu-id="5cc2e-115">PARAMETERS</span></span>

### <span data-ttu-id="5cc2e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cc2e-116">-AsJob</span></span>
<span data-ttu-id="5cc2e-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5cc2e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cc2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc2e-118">-DefaultProfile</span></span>
<span data-ttu-id="5cc2e-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5cc2e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc2e-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5cc2e-120">-KeyId</span></span>
<span data-ttu-id="5cc2e-121">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc2e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cc2e-122">-ResourceGroupName</span></span>
<span data-ttu-id="5cc2e-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5cc2e-123">The name of the resource group</span></span>

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

### <span data-ttu-id="5cc2e-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5cc2e-124">-ServerName</span></span>
<span data-ttu-id="5cc2e-125">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5cc2e-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5cc2e-126">-Confirm</span></span>
<span data-ttu-id="5cc2e-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc2e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc2e-128">-WhatIf</span></span>
<span data-ttu-id="5cc2e-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cc2e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc2e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc2e-131">CommonParameters</span></span>
<span data-ttu-id="5cc2e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cc2e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc2e-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cc2e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc2e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5cc2e-134">INPUTS</span></span>

### <span data-ttu-id="5cc2e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5cc2e-135">System.String</span></span>

## <span data-ttu-id="5cc2e-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5cc2e-136">OUTPUTS</span></span>

### <span data-ttu-id="5cc2e-137">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="5cc2e-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="5cc2e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5cc2e-138">NOTES</span></span>

## <span data-ttu-id="5cc2e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cc2e-139">RELATED LINKS</span></span>

[<span data-ttu-id="5cc2e-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5cc2e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
