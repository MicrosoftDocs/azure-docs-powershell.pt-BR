---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: e8606f9eecfac63b68e9b8a26ecbebb89431e509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602185"
---
# <span data-ttu-id="52412-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="52412-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="52412-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52412-102">SYNOPSIS</span></span>
<span data-ttu-id="52412-103">Remove uma chave do cofre de chaves de um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="52412-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52412-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52412-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52412-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52412-105">DESCRIPTION</span></span>
<span data-ttu-id="52412-106">O cmdlet Remove-AzureRmSqlServerKeyVaultKey remove a chave do cofre de chaves do SQL Server especificado.</span><span class="sxs-lookup"><span data-stu-id="52412-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="52412-107">Observe que as permissões do SQL Server para o cofre da chave não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="52412-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="52412-108">Para alterar permissões, use set-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="52412-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="52412-109">Observe que esse cmdlet não faz alterações no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="52412-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="52412-110">Para remover uma chave do cofre de chaves, use remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="52412-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="52412-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52412-111">EXAMPLES</span></span>

### <span data-ttu-id="52412-112">--------------------------Exemplo 1: remover uma chave do cofre de chaves--------------------------</span><span class="sxs-lookup"><span data-stu-id="52412-112">--------------------------  Example 1: Remove a Key Vault key  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="52412-113">Este comando Remove a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="52412-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="52412-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="52412-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="52412-115">OS</span><span class="sxs-lookup"><span data-stu-id="52412-115">PARAMETERS</span></span>

### <span data-ttu-id="52412-116">-KeyId</span><span class="sxs-lookup"><span data-stu-id="52412-116">-KeyId</span></span>
<span data-ttu-id="52412-117">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="52412-117">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="52412-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52412-118">-ResourceGroupName</span></span>
<span data-ttu-id="52412-119">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="52412-119">The name of the resource group</span></span>

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

### <span data-ttu-id="52412-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="52412-120">-ServerName</span></span>
<span data-ttu-id="52412-121">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="52412-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="52412-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52412-122">-Confirm</span></span>
<span data-ttu-id="52412-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52412-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52412-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52412-124">-WhatIf</span></span>
<span data-ttu-id="52412-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52412-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52412-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52412-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52412-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52412-127">-DefaultProfile</span></span>
<span data-ttu-id="52412-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52412-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52412-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52412-129">CommonParameters</span></span>
<span data-ttu-id="52412-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52412-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52412-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52412-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52412-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52412-132">INPUTS</span></span>

### <span data-ttu-id="52412-133">System. String</span><span class="sxs-lookup"><span data-stu-id="52412-133">System.String</span></span>

## <span data-ttu-id="52412-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52412-134">OUTPUTS</span></span>

### <span data-ttu-id="52412-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="52412-135">System.Object</span></span>

## <span data-ttu-id="52412-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52412-136">NOTES</span></span>

## <span data-ttu-id="52412-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52412-137">RELATED LINKS</span></span>

[<span data-ttu-id="52412-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="52412-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
