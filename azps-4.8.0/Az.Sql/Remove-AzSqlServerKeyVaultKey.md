---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113898"
---
# <span data-ttu-id="59681-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59681-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="59681-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59681-102">SYNOPSIS</span></span>
<span data-ttu-id="59681-103">Remove uma chave do cofre de chaves de um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="59681-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="59681-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59681-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59681-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59681-105">DESCRIPTION</span></span>
<span data-ttu-id="59681-106">O cmdlet Remove-AzSqlServerKeyVaultKey remove a chave do cofre de chaves do SQL Server especificado.</span><span class="sxs-lookup"><span data-stu-id="59681-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="59681-107">Observe que as permissões do SQL Server para o cofre da chave não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="59681-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="59681-108">Para alterar permissões, use set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="59681-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="59681-109">Observe que esse cmdlet não faz alterações no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="59681-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="59681-110">Para remover uma chave do cofre de chaves, use remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="59681-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="59681-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59681-111">EXAMPLES</span></span>

### <span data-ttu-id="59681-112">Exemplo 1: remover uma chave do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="59681-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="59681-113">Este comando Remove a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="59681-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="59681-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="59681-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="59681-115">OS</span><span class="sxs-lookup"><span data-stu-id="59681-115">PARAMETERS</span></span>

### <span data-ttu-id="59681-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59681-116">-AsJob</span></span>
<span data-ttu-id="59681-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="59681-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59681-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59681-118">-DefaultProfile</span></span>
<span data-ttu-id="59681-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="59681-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59681-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="59681-120">-KeyId</span></span>
<span data-ttu-id="59681-121">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="59681-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="59681-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59681-122">-ResourceGroupName</span></span>
<span data-ttu-id="59681-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="59681-123">The name of the resource group</span></span>

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

### <span data-ttu-id="59681-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="59681-124">-ServerName</span></span>
<span data-ttu-id="59681-125">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="59681-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="59681-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59681-126">-Confirm</span></span>
<span data-ttu-id="59681-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59681-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59681-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59681-128">-WhatIf</span></span>
<span data-ttu-id="59681-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59681-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59681-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59681-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59681-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59681-131">CommonParameters</span></span>
<span data-ttu-id="59681-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59681-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59681-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59681-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59681-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59681-134">INPUTS</span></span>

### <span data-ttu-id="59681-135">System. String</span><span class="sxs-lookup"><span data-stu-id="59681-135">System.String</span></span>

## <span data-ttu-id="59681-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59681-136">OUTPUTS</span></span>

### <span data-ttu-id="59681-137">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="59681-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="59681-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59681-138">NOTES</span></span>

## <span data-ttu-id="59681-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59681-139">RELATED LINKS</span></span>

[<span data-ttu-id="59681-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="59681-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
