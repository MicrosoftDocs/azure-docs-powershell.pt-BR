---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 4f26955db9d99871cb0c5ae127b5977deedacf08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426561"
---
# <span data-ttu-id="533a1-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="533a1-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="533a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="533a1-102">SYNOPSIS</span></span>
<span data-ttu-id="533a1-103">Obtém as chaves do cofre de chaves do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="533a1-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="533a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="533a1-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="533a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="533a1-105">DESCRIPTION</span></span>
<span data-ttu-id="533a1-106">O cmdlet Get-AzureRmSqlServerKeyVaultKey Obtém informações sobre as chaves do cofre de chaves em um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="533a1-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="533a1-107">Você pode exibir todas as chaves em um servidor ou exibir uma chave específica fornecendo o KeyId.</span><span class="sxs-lookup"><span data-stu-id="533a1-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="533a1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="533a1-108">EXAMPLES</span></span>

### <span data-ttu-id="533a1-109">Exemplo 1: obter todas as chaves do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="533a1-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="533a1-110">Esse comando obtém todas as chaves do cofre de chaves em um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="533a1-110">This command gets all the Key Vault keys on a SQL server.</span></span>

<span data-ttu-id="533a1-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="533a1-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

<span data-ttu-id="533a1-112">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey2_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="533a1-112">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="533a1-113">Exemplo 2: obter uma chave específica do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="533a1-113">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="533a1-114">Este comando obtém a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' e, em seguida, armazena-a na variável $MyServerKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="533a1-114">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="533a1-115">Você pode inspecionar as propriedades de $MyServerKeyVaultKey para obter detalhes sobre o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="533a1-115">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="533a1-116">OS</span><span class="sxs-lookup"><span data-stu-id="533a1-116">PARAMETERS</span></span>

### <span data-ttu-id="533a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="533a1-117">-DefaultProfile</span></span>
<span data-ttu-id="533a1-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="533a1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="533a1-119">-KeyId</span><span class="sxs-lookup"><span data-stu-id="533a1-119">-KeyId</span></span>
<span data-ttu-id="533a1-120">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="533a1-120">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="533a1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="533a1-121">-ResourceGroupName</span></span>
<span data-ttu-id="533a1-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="533a1-122">The name of the resource group</span></span>

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

### <span data-ttu-id="533a1-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="533a1-123">-ServerName</span></span>
<span data-ttu-id="533a1-124">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="533a1-124">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="533a1-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="533a1-125">-Confirm</span></span>
<span data-ttu-id="533a1-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="533a1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="533a1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="533a1-127">-WhatIf</span></span>
<span data-ttu-id="533a1-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="533a1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="533a1-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="533a1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="533a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="533a1-130">CommonParameters</span></span>
<span data-ttu-id="533a1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="533a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="533a1-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="533a1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="533a1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="533a1-133">INPUTS</span></span>

### <span data-ttu-id="533a1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="533a1-134">System.String</span></span>

## <span data-ttu-id="533a1-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="533a1-135">OUTPUTS</span></span>

### <span data-ttu-id="533a1-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="533a1-136">System.Object</span></span>

## <span data-ttu-id="533a1-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="533a1-137">NOTES</span></span>

## <span data-ttu-id="533a1-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="533a1-138">RELATED LINKS</span></span>

[<span data-ttu-id="533a1-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="533a1-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
