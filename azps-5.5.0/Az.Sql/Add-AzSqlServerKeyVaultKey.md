---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112563"
---
# <span data-ttu-id="f7401-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f7401-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="f7401-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7401-102">SYNOPSIS</span></span>
<span data-ttu-id="f7401-103">Adiciona uma chave do Cofre de Teclas a um servidor SQL.</span><span class="sxs-lookup"><span data-stu-id="f7401-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="f7401-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7401-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7401-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7401-105">DESCRIPTION</span></span>
<span data-ttu-id="f7401-106">O cmdlet Add-AzSqlServerKeyVaultKey adiciona uma chave do Cofre de Teclas ao servidor SQL fornecido.</span><span class="sxs-lookup"><span data-stu-id="f7401-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="f7401-107">O servidor deve ter permissões 'get, wrapKey, unwrapKey' para o cofre.</span><span class="sxs-lookup"><span data-stu-id="f7401-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="f7401-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7401-108">EXAMPLES</span></span>

### <span data-ttu-id="f7401-109">Exemplo 1: Adicionar chave do Cofre de Teclas</span><span class="sxs-lookup"><span data-stu-id="f7401-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="f7401-110">Esse comando adiciona a chave do Cofre de Teclas com Id ' ao servidor SQL chamado 'ContosoServer' no grupo de recursos https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="f7401-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="f7401-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 : Thumbprint : 1122334456778899001122344556677889900 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="f7401-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="f7401-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7401-112">PARAMETERS</span></span>

### <span data-ttu-id="f7401-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7401-113">-AsJob</span></span>
<span data-ttu-id="f7401-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f7401-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7401-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7401-115">-DefaultProfile</span></span>
<span data-ttu-id="f7401-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f7401-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7401-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f7401-117">-KeyId</span></span>
<span data-ttu-id="f7401-118">A KeyId do Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7401-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="f7401-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7401-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7401-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f7401-120">The name of the resource group</span></span>

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

### <span data-ttu-id="f7401-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f7401-121">-ServerName</span></span>
<span data-ttu-id="f7401-122">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7401-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f7401-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f7401-123">-Confirm</span></span>
<span data-ttu-id="f7401-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7401-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7401-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7401-125">-WhatIf</span></span>
<span data-ttu-id="f7401-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f7401-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7401-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7401-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7401-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7401-128">CommonParameters</span></span>
<span data-ttu-id="f7401-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7401-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7401-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7401-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7401-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="f7401-131">INPUTS</span></span>

### <span data-ttu-id="f7401-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f7401-132">System.String</span></span>

## <span data-ttu-id="f7401-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="f7401-133">OUTPUTS</span></span>

### <span data-ttu-id="f7401-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="f7401-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="f7401-135">Notas</span><span class="sxs-lookup"><span data-stu-id="f7401-135">NOTES</span></span>

## <span data-ttu-id="f7401-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7401-136">RELATED LINKS</span></span>

[<span data-ttu-id="f7401-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f7401-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
