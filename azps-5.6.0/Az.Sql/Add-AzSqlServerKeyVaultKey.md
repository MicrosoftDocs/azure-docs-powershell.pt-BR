---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f354fe8ad1876eb756cdf78378dbf7048e53932d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886570"
---
# <span data-ttu-id="42f23-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="42f23-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="42f23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42f23-102">SYNOPSIS</span></span>
<span data-ttu-id="42f23-103">Adiciona uma chave do Cofre de Chaves a um SQL servidor.</span><span class="sxs-lookup"><span data-stu-id="42f23-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="42f23-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="42f23-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42f23-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="42f23-105">DESCRIPTION</span></span>
<span data-ttu-id="42f23-106">O Add-AzSqlServerKeyVaultKey cmdlet adiciona uma chave do Cofre de Chaves ao servidor SQL fornecido.</span><span class="sxs-lookup"><span data-stu-id="42f23-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="42f23-107">O servidor deve ter permissões 'get, wrapKey, unwrapKey' para o cofre.</span><span class="sxs-lookup"><span data-stu-id="42f23-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="42f23-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42f23-108">EXAMPLES</span></span>

### <span data-ttu-id="42f23-109">Exemplo 1: Adicionar chave do Cofre de Chaves</span><span class="sxs-lookup"><span data-stu-id="42f23-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="42f23-110">Este comando adiciona a chave do Cofre de Chaves com Id ' ' ao servidor SQL chamado 'ContosoServer' no grupo de recursos https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 'ContosoResourceGroup'.</span><span class="sxs-lookup"><span data-stu-id="42f23-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="42f23-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Tipo : AzureKeyVault Uri : Impressão digital https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 : 112233445667788899001122334456677889900 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="42f23-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="42f23-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="42f23-112">PARAMETERS</span></span>

### <span data-ttu-id="42f23-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42f23-113">-AsJob</span></span>
<span data-ttu-id="42f23-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="42f23-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42f23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f23-115">-DefaultProfile</span></span>
<span data-ttu-id="42f23-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="42f23-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42f23-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="42f23-117">-KeyId</span></span>
<span data-ttu-id="42f23-118">KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="42f23-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="42f23-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f23-119">-ResourceGroupName</span></span>
<span data-ttu-id="42f23-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="42f23-120">The name of the resource group</span></span>

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

### <span data-ttu-id="42f23-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42f23-121">-ServerName</span></span>
<span data-ttu-id="42f23-122">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="42f23-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="42f23-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42f23-123">-Confirm</span></span>
<span data-ttu-id="42f23-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42f23-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42f23-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42f23-125">-WhatIf</span></span>
<span data-ttu-id="42f23-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42f23-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42f23-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42f23-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42f23-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f23-128">CommonParameters</span></span>
<span data-ttu-id="42f23-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f23-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f23-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42f23-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f23-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42f23-131">INPUTS</span></span>

### <span data-ttu-id="42f23-132">System.String</span><span class="sxs-lookup"><span data-stu-id="42f23-132">System.String</span></span>

## <span data-ttu-id="42f23-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="42f23-133">OUTPUTS</span></span>

### <span data-ttu-id="42f23-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="42f23-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="42f23-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="42f23-135">NOTES</span></span>

## <span data-ttu-id="42f23-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42f23-136">RELATED LINKS</span></span>

[<span data-ttu-id="42f23-137">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="42f23-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
