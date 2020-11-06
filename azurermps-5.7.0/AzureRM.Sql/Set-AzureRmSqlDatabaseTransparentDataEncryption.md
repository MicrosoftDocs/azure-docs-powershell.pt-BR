---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 0b2a9174f90ece49f417dd413e23da786b983a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427421"
---
# <span data-ttu-id="c5e77-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c5e77-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="c5e77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5e77-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e77-103">Modifica a propriedade TDE de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c5e77-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5e77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5e77-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e77-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5e77-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e77-106">O cmdlet **set-AzureRmSqlDatabaseTransparentDataEncryption** modifica a propriedade de criptografia de dados transparente (TDE) de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c5e77-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="c5e77-107">Para obter mais informações, consulte criptografia de dados transparente com o banco de dados SQL do Azure https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) na biblioteca do Microsoft Developer Network).</span><span class="sxs-lookup"><span data-stu-id="c5e77-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="c5e77-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="c5e77-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c5e77-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5e77-109">EXAMPLES</span></span>

### <span data-ttu-id="c5e77-110">Exemplo 1: habilitar o TDE para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="c5e77-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="c5e77-111">Esse comando habilita TDE para o banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="c5e77-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="c5e77-112">OS</span><span class="sxs-lookup"><span data-stu-id="c5e77-112">PARAMETERS</span></span>

### <span data-ttu-id="c5e77-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c5e77-113">-DatabaseName</span></span>
<span data-ttu-id="c5e77-114">Especifica o nome do banco de dados que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="c5e77-114">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e77-115">-DefaultProfile</span></span>
<span data-ttu-id="c5e77-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c5e77-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5e77-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e77-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5e77-118">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c5e77-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c5e77-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c5e77-119">-ServerName</span></span>
<span data-ttu-id="c5e77-120">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c5e77-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="c5e77-121">-Estado</span><span class="sxs-lookup"><span data-stu-id="c5e77-121">-State</span></span>
<span data-ttu-id="c5e77-122">Especifica o valor da propriedade TDE.</span><span class="sxs-lookup"><span data-stu-id="c5e77-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="c5e77-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c5e77-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c5e77-124">Possibilita</span><span class="sxs-lookup"><span data-stu-id="c5e77-124">Enabled</span></span> 
- <span data-ttu-id="c5e77-125">Ativo</span><span class="sxs-lookup"><span data-stu-id="c5e77-125">Disabled</span></span>

```yaml
Type: TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e77-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5e77-126">-Confirm</span></span>
<span data-ttu-id="c5e77-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e77-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e77-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e77-128">-WhatIf</span></span>
<span data-ttu-id="c5e77-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5e77-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e77-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5e77-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e77-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e77-131">CommonParameters</span></span>
<span data-ttu-id="c5e77-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e77-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e77-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e77-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e77-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5e77-134">INPUTS</span></span>

### <span data-ttu-id="c5e77-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c5e77-135">None</span></span>
<span data-ttu-id="c5e77-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c5e77-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5e77-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5e77-137">OUTPUTS</span></span>

### <span data-ttu-id="c5e77-138">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="c5e77-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="c5e77-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5e77-139">NOTES</span></span>

## <span data-ttu-id="c5e77-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5e77-140">RELATED LINKS</span></span>

[<span data-ttu-id="c5e77-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c5e77-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="c5e77-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="c5e77-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="c5e77-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="c5e77-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


