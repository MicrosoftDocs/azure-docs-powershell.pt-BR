---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 6cc3b0f066f267b51a90c0cb0c56d1972ec92f5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773870"
---
# <span data-ttu-id="590e2-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="590e2-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="590e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="590e2-102">SYNOPSIS</span></span>
<span data-ttu-id="590e2-103">Obtém as chaves do cofre de chaves do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="590e2-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="590e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="590e2-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="590e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="590e2-105">DESCRIPTION</span></span>
<span data-ttu-id="590e2-106">O cmdlet Get-AzSqlServerKeyVaultKey Obtém informações sobre as chaves do cofre de chaves em um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="590e2-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="590e2-107">Você pode exibir todas as chaves em um servidor ou exibir uma chave específica fornecendo o KeyId.</span><span class="sxs-lookup"><span data-stu-id="590e2-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="590e2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="590e2-108">EXAMPLES</span></span>

### <span data-ttu-id="590e2-109">Exemplo 1: obter todas as chaves do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="590e2-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="590e2-110">Esse comando obtém todas as chaves do cofre de chaves em um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="590e2-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="590e2-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am ResourceGroupName: ContosoResourceGroup nome_do_servidor: ContosoServer ServerKeyName: Contoso_contosokey2_01234567890123456789012345678901 Type: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="590e2-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="590e2-112">Exemplo 2: obter uma chave específica do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="590e2-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="590e2-113">Este comando obtém a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' e, em seguida, armazena-a na variável $MyServerKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="590e2-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="590e2-114">Você pode inspecionar as propriedades de $MyServerKeyVaultKey para obter detalhes sobre o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="590e2-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="590e2-115">OS</span><span class="sxs-lookup"><span data-stu-id="590e2-115">PARAMETERS</span></span>

### <span data-ttu-id="590e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590e2-116">-DefaultProfile</span></span>
<span data-ttu-id="590e2-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="590e2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="590e2-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="590e2-118">-KeyId</span></span>
<span data-ttu-id="590e2-119">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="590e2-119">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="590e2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="590e2-120">-ResourceGroupName</span></span>
<span data-ttu-id="590e2-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="590e2-121">The name of the resource group</span></span>

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

### <span data-ttu-id="590e2-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="590e2-122">-ServerName</span></span>
<span data-ttu-id="590e2-123">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="590e2-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="590e2-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="590e2-124">-Confirm</span></span>
<span data-ttu-id="590e2-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="590e2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="590e2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="590e2-126">-WhatIf</span></span>
<span data-ttu-id="590e2-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="590e2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="590e2-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="590e2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="590e2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590e2-129">CommonParameters</span></span>
<span data-ttu-id="590e2-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="590e2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590e2-131">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="590e2-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590e2-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="590e2-132">INPUTS</span></span>

### <span data-ttu-id="590e2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="590e2-133">System.String</span></span>

## <span data-ttu-id="590e2-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="590e2-134">OUTPUTS</span></span>

### <span data-ttu-id="590e2-135">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="590e2-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="590e2-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="590e2-136">NOTES</span></span>

## <span data-ttu-id="590e2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="590e2-137">RELATED LINKS</span></span>

[<span data-ttu-id="590e2-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="590e2-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)