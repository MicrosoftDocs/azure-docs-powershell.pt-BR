---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 333e4b1e5f01c76947ca32277fd8ca7ff75218eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602347"
---
# <span data-ttu-id="4946b-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4946b-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="4946b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4946b-102">SYNOPSIS</span></span>
<span data-ttu-id="4946b-103">Remove uma chave do cofre de chaves de um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4946b-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4946b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4946b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4946b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4946b-105">DESCRIPTION</span></span>
<span data-ttu-id="4946b-106">O cmdlet Remove-AzureRmSqlServerKeyVaultKey remove a chave do cofre de chaves do SQL Server especificado.</span><span class="sxs-lookup"><span data-stu-id="4946b-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="4946b-107">Observe que as permissões do SQL Server para o cofre da chave não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="4946b-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="4946b-108">Para alterar permissões, use set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="4946b-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="4946b-109">Observe que esse cmdlet não faz alterações no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4946b-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="4946b-110">Para remover uma chave do cofre de chaves, use remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="4946b-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="4946b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4946b-111">EXAMPLES</span></span>

### <span data-ttu-id="4946b-112">Exemplo 1: remover uma chave do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="4946b-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="4946b-113">Este comando Remove a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="4946b-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="4946b-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="4946b-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="4946b-115">OS</span><span class="sxs-lookup"><span data-stu-id="4946b-115">PARAMETERS</span></span>

### <span data-ttu-id="4946b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4946b-116">-AsJob</span></span>
<span data-ttu-id="4946b-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4946b-117">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="4946b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4946b-118">-DefaultProfile</span></span>
<span data-ttu-id="4946b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4946b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4946b-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4946b-120">-KeyId</span></span>
<span data-ttu-id="4946b-121">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4946b-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4946b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4946b-122">-ResourceGroupName</span></span>
<span data-ttu-id="4946b-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4946b-123">The name of the resource group</span></span>

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

### <span data-ttu-id="4946b-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4946b-124">-ServerName</span></span>
<span data-ttu-id="4946b-125">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="4946b-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4946b-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4946b-126">-Confirm</span></span>
<span data-ttu-id="4946b-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4946b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4946b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4946b-128">-WhatIf</span></span>
<span data-ttu-id="4946b-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4946b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4946b-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4946b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4946b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4946b-131">CommonParameters</span></span>
<span data-ttu-id="4946b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4946b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4946b-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4946b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4946b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4946b-134">INPUTS</span></span>

### <span data-ttu-id="4946b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4946b-135">System.String</span></span>

## <span data-ttu-id="4946b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4946b-136">OUTPUTS</span></span>

### <span data-ttu-id="4946b-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="4946b-137">System.Object</span></span>

## <span data-ttu-id="4946b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4946b-138">NOTES</span></span>

## <span data-ttu-id="4946b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4946b-139">RELATED LINKS</span></span>

[<span data-ttu-id="4946b-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4946b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
