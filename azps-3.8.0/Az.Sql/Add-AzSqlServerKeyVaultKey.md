---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941267"
---
# <span data-ttu-id="5377c-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5377c-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="5377c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5377c-102">SYNOPSIS</span></span>
<span data-ttu-id="5377c-103">Adiciona uma chave do cofre de chaves a um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5377c-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="5377c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5377c-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5377c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5377c-105">DESCRIPTION</span></span>
<span data-ttu-id="5377c-106">O cmdlet Add-AzSqlServerKeyVaultKey adiciona uma chave do cofre de chaves ao SQL Server fornecido.</span><span class="sxs-lookup"><span data-stu-id="5377c-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="5377c-107">O servidor deve ter as permissões ' Get, wrapKey, unwrapKey ' para o cofre.</span><span class="sxs-lookup"><span data-stu-id="5377c-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="5377c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5377c-108">EXAMPLES</span></span>

### <span data-ttu-id="5377c-109">Exemplo 1: Adicionar chave do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="5377c-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="5377c-110">Esse comando adiciona a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ao SQL Server chamado ' ContosoServer ' no grupo de recursos ' ContosoResourceGroup '.</span><span class="sxs-lookup"><span data-stu-id="5377c-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="5377c-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="5377c-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="5377c-112">OS</span><span class="sxs-lookup"><span data-stu-id="5377c-112">PARAMETERS</span></span>

### <span data-ttu-id="5377c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5377c-113">-AsJob</span></span>
<span data-ttu-id="5377c-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5377c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5377c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5377c-115">-DefaultProfile</span></span>
<span data-ttu-id="5377c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5377c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5377c-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5377c-117">-KeyId</span></span>
<span data-ttu-id="5377c-118">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5377c-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="5377c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5377c-119">-ResourceGroupName</span></span>
<span data-ttu-id="5377c-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5377c-120">The name of the resource group</span></span>

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

### <span data-ttu-id="5377c-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5377c-121">-ServerName</span></span>
<span data-ttu-id="5377c-122">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="5377c-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5377c-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5377c-123">-Confirm</span></span>
<span data-ttu-id="5377c-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5377c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5377c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5377c-125">-WhatIf</span></span>
<span data-ttu-id="5377c-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5377c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5377c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5377c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5377c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5377c-128">CommonParameters</span></span>
<span data-ttu-id="5377c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5377c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5377c-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5377c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5377c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5377c-131">INPUTS</span></span>

### <span data-ttu-id="5377c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5377c-132">System.String</span></span>

## <span data-ttu-id="5377c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5377c-133">OUTPUTS</span></span>

### <span data-ttu-id="5377c-134">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="5377c-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="5377c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5377c-135">NOTES</span></span>

## <span data-ttu-id="5377c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5377c-136">RELATED LINKS</span></span>

[<span data-ttu-id="5377c-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5377c-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
