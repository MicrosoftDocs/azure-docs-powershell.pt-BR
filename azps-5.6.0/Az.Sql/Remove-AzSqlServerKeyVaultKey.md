---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 5b394909df0469c37a0217b3eb861ce4a1146e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887304"
---
# <span data-ttu-id="b6479-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b6479-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="b6479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6479-102">SYNOPSIS</span></span>
<span data-ttu-id="b6479-103">Remove uma chave do Cofre de Chaves de um SQL servidor.</span><span class="sxs-lookup"><span data-stu-id="b6479-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="b6479-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b6479-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6479-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b6479-105">DESCRIPTION</span></span>
<span data-ttu-id="b6479-106">O Remove-AzSqlServerKeyVaultKey cmdlet remove a tecla Key Vault do servidor SQL especificado.</span><span class="sxs-lookup"><span data-stu-id="b6479-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="b6479-107">Observe que SQL permissões do servidor para o cofre da chave não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="b6479-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="b6479-108">Para alterar permissões, use Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="b6479-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="b6479-109">Observe que este cmdlet não faz alterações no Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="b6479-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="b6479-110">Para remover uma chave do Cofre de Chaves, use Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="b6479-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="b6479-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6479-111">EXAMPLES</span></span>

### <span data-ttu-id="b6479-112">Exemplo 1: Remover uma chave do Cofre de Chaves</span><span class="sxs-lookup"><span data-stu-id="b6479-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="b6479-113">Este comando remove a tecla Key Vault com Id ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="b6479-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="b6479-114">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Tipo : AzureKeyVault Uri : Impressão digital https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 : 112233445667788899001122334456677889900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="b6479-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="b6479-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b6479-115">PARAMETERS</span></span>

### <span data-ttu-id="b6479-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6479-116">-AsJob</span></span>
<span data-ttu-id="b6479-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b6479-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6479-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6479-118">-DefaultProfile</span></span>
<span data-ttu-id="b6479-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b6479-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6479-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b6479-120">-KeyId</span></span>
<span data-ttu-id="b6479-121">KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b6479-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="b6479-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6479-122">-ResourceGroupName</span></span>
<span data-ttu-id="b6479-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b6479-123">The name of the resource group</span></span>

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

### <span data-ttu-id="b6479-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b6479-124">-ServerName</span></span>
<span data-ttu-id="b6479-125">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="b6479-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b6479-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6479-126">-Confirm</span></span>
<span data-ttu-id="b6479-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6479-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6479-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6479-128">-WhatIf</span></span>
<span data-ttu-id="b6479-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6479-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6479-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6479-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6479-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6479-131">CommonParameters</span></span>
<span data-ttu-id="b6479-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6479-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6479-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6479-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6479-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6479-134">INPUTS</span></span>

### <span data-ttu-id="b6479-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b6479-135">System.String</span></span>

## <span data-ttu-id="b6479-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b6479-136">OUTPUTS</span></span>

### <span data-ttu-id="b6479-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="b6479-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="b6479-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="b6479-138">NOTES</span></span>

## <span data-ttu-id="b6479-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6479-139">RELATED LINKS</span></span>

[<span data-ttu-id="b6479-140">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="b6479-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
