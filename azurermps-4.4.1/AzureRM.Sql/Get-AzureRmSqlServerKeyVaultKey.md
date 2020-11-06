---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 17022a34ad8a5f2be673243e9dcb6c7063c8fbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429039"
---
# <span data-ttu-id="7480c-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7480c-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="7480c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7480c-102">SYNOPSIS</span></span>
<span data-ttu-id="7480c-103">Obtém as chaves do cofre de chaves do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7480c-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7480c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7480c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7480c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7480c-105">DESCRIPTION</span></span>
<span data-ttu-id="7480c-106">O cmdlet Get-AzureRmSqlServerKeyVaultKey Obtém informações sobre as chaves do cofre de chaves em um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7480c-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="7480c-107">Você pode exibir todas as chaves em um servidor ou exibir uma chave específica fornecendo o KeyId.</span><span class="sxs-lookup"><span data-stu-id="7480c-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="7480c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7480c-108">EXAMPLES</span></span>

### <span data-ttu-id="7480c-109">--------------------------Exemplo 1: obter todas as chaves de compartimento de chave--------------------------</span><span class="sxs-lookup"><span data-stu-id="7480c-109">--------------------------  Example 1: Get all Key Vault keys  --------------------------</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="7480c-110">Esse comando obtém todas as chaves do cofre de chaves em um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7480c-110">This command gets all the Key Vault keys on a SQL server.</span></span>

<span data-ttu-id="7480c-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="7480c-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

<span data-ttu-id="7480c-112">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey2_01234567890123456789012345678901 tipo: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="7480c-112">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="7480c-113">--------------------------Exemplo 2: obter uma chave do cofre de chaves específica--------------------------</span><span class="sxs-lookup"><span data-stu-id="7480c-113">--------------------------  Example 2: Get a specific Key Vault key  --------------------------</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="7480c-114">Este comando obtém a chave do cofre de chaves com ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' e, em seguida, armazena-a na variável $MyServerKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="7480c-114">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="7480c-115">Você pode inspecionar as propriedades de $MyServerKeyVaultKey para obter detalhes sobre o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7480c-115">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="7480c-116">OS</span><span class="sxs-lookup"><span data-stu-id="7480c-116">PARAMETERS</span></span>

### <span data-ttu-id="7480c-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7480c-117">-KeyId</span></span>
<span data-ttu-id="7480c-118">O KeyId do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7480c-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="7480c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7480c-119">-ResourceGroupName</span></span>
<span data-ttu-id="7480c-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7480c-120">The name of the resource group</span></span>

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

### <span data-ttu-id="7480c-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7480c-121">-ServerName</span></span>
<span data-ttu-id="7480c-122">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="7480c-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7480c-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7480c-123">-Confirm</span></span>
<span data-ttu-id="7480c-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7480c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7480c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7480c-125">-WhatIf</span></span>
<span data-ttu-id="7480c-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7480c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7480c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7480c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7480c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7480c-128">-DefaultProfile</span></span>
<span data-ttu-id="7480c-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7480c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7480c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7480c-130">CommonParameters</span></span>
<span data-ttu-id="7480c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7480c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7480c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7480c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7480c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7480c-133">INPUTS</span></span>

### <span data-ttu-id="7480c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7480c-134">System.String</span></span>

## <span data-ttu-id="7480c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7480c-135">OUTPUTS</span></span>

### <span data-ttu-id="7480c-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="7480c-136">System.Object</span></span>

## <span data-ttu-id="7480c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7480c-137">NOTES</span></span>

## <span data-ttu-id="7480c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7480c-138">RELATED LINKS</span></span>

[<span data-ttu-id="7480c-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7480c-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
