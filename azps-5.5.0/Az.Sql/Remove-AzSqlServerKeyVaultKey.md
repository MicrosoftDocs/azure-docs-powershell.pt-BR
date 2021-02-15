---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116130"
---
# <span data-ttu-id="e3ba2-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e3ba2-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="e3ba2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ba2-103">Remove uma chave do Cofre de Teclas de um servidor SQL.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="e3ba2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3ba2-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3ba2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3ba2-105">DESCRIPTION</span></span>
<span data-ttu-id="e3ba2-106">O Remove-AzSqlServerKeyVaultKey cmdlet remove a tecla Key Vault do servidor SQL especificado.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="e3ba2-107">Observe que as permissões do sql server para o cofre da chave não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="e3ba2-108">Para alterar as permissões, use Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="e3ba2-109">Observe que esse cmdlet não faz alterações no Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="e3ba2-110">Para remover uma chave do Cofre de Teclas, use Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="e3ba2-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3ba2-111">EXAMPLES</span></span>

### <span data-ttu-id="e3ba2-112">Exemplo 1: Remover uma tecla do Cofre de Teclas</span><span class="sxs-lookup"><span data-stu-id="e3ba2-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="e3ba2-113">Esse comando remove a tecla Key Vault com Id ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="e3ba2-114">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 : Thumbprint : 1122334456778899001122344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="e3ba2-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="e3ba2-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3ba2-115">PARAMETERS</span></span>

### <span data-ttu-id="e3ba2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3ba2-116">-AsJob</span></span>
<span data-ttu-id="e3ba2-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e3ba2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3ba2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ba2-118">-DefaultProfile</span></span>
<span data-ttu-id="e3ba2-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e3ba2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3ba2-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e3ba2-120">-KeyId</span></span>
<span data-ttu-id="e3ba2-121">A KeyId do Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="e3ba2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ba2-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3ba2-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e3ba2-123">The name of the resource group</span></span>

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

### <span data-ttu-id="e3ba2-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e3ba2-124">-ServerName</span></span>
<span data-ttu-id="e3ba2-125">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e3ba2-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e3ba2-126">-Confirm</span></span>
<span data-ttu-id="e3ba2-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3ba2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ba2-128">-WhatIf</span></span>
<span data-ttu-id="e3ba2-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3ba2-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3ba2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ba2-131">CommonParameters</span></span>
<span data-ttu-id="e3ba2-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3ba2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ba2-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3ba2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ba2-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="e3ba2-134">INPUTS</span></span>

### <span data-ttu-id="e3ba2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e3ba2-135">System.String</span></span>

## <span data-ttu-id="e3ba2-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="e3ba2-136">OUTPUTS</span></span>

### <span data-ttu-id="e3ba2-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="e3ba2-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="e3ba2-138">Notas</span><span class="sxs-lookup"><span data-stu-id="e3ba2-138">NOTES</span></span>

## <span data-ttu-id="e3ba2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3ba2-139">RELATED LINKS</span></span>

[<span data-ttu-id="e3ba2-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e3ba2-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
