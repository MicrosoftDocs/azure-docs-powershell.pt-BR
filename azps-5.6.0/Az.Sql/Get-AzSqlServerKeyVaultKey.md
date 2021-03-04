---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 523192b1632bf6ed67dff170b2ac94374c443299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891279"
---
# <span data-ttu-id="a0218-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a0218-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="a0218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0218-102">SYNOPSIS</span></span>
<span data-ttu-id="a0218-103">Obtém SQL chaves do Cofre de Chaves do servidor.</span><span class="sxs-lookup"><span data-stu-id="a0218-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="a0218-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a0218-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0218-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a0218-105">DESCRIPTION</span></span>
<span data-ttu-id="a0218-106">O Get-AzSqlServerKeyVaultKey cmdlet obtém informações sobre as chaves do Cofre de Chaves em um SQL servidor.</span><span class="sxs-lookup"><span data-stu-id="a0218-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="a0218-107">Você pode exibir todas as chaves em um servidor ou exibir uma chave específica fornecendo o KeyId.</span><span class="sxs-lookup"><span data-stu-id="a0218-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="a0218-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0218-108">EXAMPLES</span></span>

### <span data-ttu-id="a0218-109">Exemplo 1: Obter todas as chaves do Cofre de Chaves</span><span class="sxs-lookup"><span data-stu-id="a0218-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="a0218-110">Este comando obtém todas as chaves do Cofre de Chaves em um SQL servidor.</span><span class="sxs-lookup"><span data-stu-id="a0218-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="a0218-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Tipo : AzureKeyVault Uri : impressão digital https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 : 112233445667788899001122334456677889900 CreationDate : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey2_01234567890123456789012345678901 Tipo : AzureKeyVault Uri : Impressão digital https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 : 009987766544433221100998876654433211 CreationDate : 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="a0218-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="a0218-112">Exemplo 2: Obter uma chave específica do Cofre de Chaves</span><span class="sxs-lookup"><span data-stu-id="a0218-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="a0218-113">Este comando obtém a chave do Cofre de Chaves com id ' ', e, em seguida, armazena-a https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 na variável $MyServerKeyVaultKey chave.</span><span class="sxs-lookup"><span data-stu-id="a0218-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="a0218-114">Você pode inspecionar as propriedades do $MyServerKeyVaultKey para obter detalhes sobre o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a0218-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="a0218-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a0218-115">PARAMETERS</span></span>

### <span data-ttu-id="a0218-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0218-116">-DefaultProfile</span></span>
<span data-ttu-id="a0218-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a0218-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0218-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a0218-118">-KeyId</span></span>
<span data-ttu-id="a0218-119">KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a0218-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0218-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0218-120">-ResourceGroupName</span></span>
<span data-ttu-id="a0218-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a0218-121">The name of the resource group</span></span>

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

### <span data-ttu-id="a0218-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0218-122">-ServerName</span></span>
<span data-ttu-id="a0218-123">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0218-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a0218-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0218-124">-Confirm</span></span>
<span data-ttu-id="a0218-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0218-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0218-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0218-126">-WhatIf</span></span>
<span data-ttu-id="a0218-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0218-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0218-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0218-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0218-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0218-129">CommonParameters</span></span>
<span data-ttu-id="a0218-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0218-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0218-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0218-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0218-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0218-132">INPUTS</span></span>

### <span data-ttu-id="a0218-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a0218-133">System.String</span></span>

## <span data-ttu-id="a0218-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a0218-134">OUTPUTS</span></span>

### <span data-ttu-id="a0218-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="a0218-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="a0218-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="a0218-136">NOTES</span></span>

## <span data-ttu-id="a0218-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0218-137">RELATED LINKS</span></span>

[<span data-ttu-id="a0218-138">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="a0218-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
