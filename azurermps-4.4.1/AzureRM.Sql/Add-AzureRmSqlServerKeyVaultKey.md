---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: b9051f8729ae1cee8216de5d2dab6d5ceb79a717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440938"
---
# <span data-ttu-id="e873e-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e873e-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="e873e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e873e-102">SYNOPSIS</span></span>
<span data-ttu-id="e873e-103">Adiciona uma chave do cofre de chaves a um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e873e-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e873e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e873e-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e873e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e873e-105">DESCRIPTION</span></span>
<span data-ttu-id="e873e-106">O cmdlet Add-AzureRmSqlServerKeyVaultKey adiciona uma chave do cofre de chaves ao SQL Server fornecido.</span><span class="sxs-lookup"><span data-stu-id="e873e-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="e873e-107">O servidor deve ter as permissões ' Get, wrapKey, unwrapKey ' para o cofre.</span><span class="sxs-lookup"><span data-stu-id="e873e-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="e873e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e873e-108">EXAMPLES</span></span>

### <span data-ttu-id="e873e-109">--------------------------Exemplo 1: Adicionar chave do cofre de chaves--------------------------</span><span class="sxs-lookup"><span data-stu-id="e873e-109">--------------------------  Example 1: Add Key Vault key  --------------------------</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="e873e-110">Esse comando adiciona a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ao SQL Server chamado ' ContosoServer ' no grupo de recursos ' ContosoResourceGroup '.</span><span class="sxs-lookup"><span data-stu-id="e873e-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="e873e-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="e873e-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="e873e-112">OS</span><span class="sxs-lookup"><span data-stu-id="e873e-112">PARAMETERS</span></span>

### <span data-ttu-id="e873e-113">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e873e-113">-KeyId</span></span>
<span data-ttu-id="e873e-114">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e873e-114">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="e873e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e873e-115">-ResourceGroupName</span></span>
<span data-ttu-id="e873e-116">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e873e-116">The name of the resource group</span></span>

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

### <span data-ttu-id="e873e-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e873e-117">-ServerName</span></span>
<span data-ttu-id="e873e-118">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="e873e-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e873e-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e873e-119">-Confirm</span></span>
<span data-ttu-id="e873e-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e873e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e873e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e873e-121">-WhatIf</span></span>
<span data-ttu-id="e873e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e873e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e873e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e873e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e873e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e873e-124">-DefaultProfile</span></span>
<span data-ttu-id="e873e-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e873e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e873e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e873e-126">CommonParameters</span></span>
<span data-ttu-id="e873e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e873e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e873e-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e873e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e873e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e873e-129">INPUTS</span></span>

### <span data-ttu-id="e873e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e873e-130">System.String</span></span>

## <span data-ttu-id="e873e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e873e-131">OUTPUTS</span></span>

### <span data-ttu-id="e873e-132">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="e873e-132">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="e873e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e873e-133">NOTES</span></span>

## <span data-ttu-id="e873e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e873e-134">RELATED LINKS</span></span>

[<span data-ttu-id="e873e-135">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e873e-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
