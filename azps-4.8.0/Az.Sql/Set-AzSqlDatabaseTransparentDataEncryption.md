---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: f2e9cc38faab0af87eb20b3a60d61ab679c435d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954565"
---
# <span data-ttu-id="8185e-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="8185e-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="8185e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8185e-102">SYNOPSIS</span></span>
<span data-ttu-id="8185e-103">Modifica a propriedade TDE de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8185e-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="8185e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8185e-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8185e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8185e-105">DESCRIPTION</span></span>
<span data-ttu-id="8185e-106">O cmdlet **set-AzSqlDatabaseTransparentDataEncryption** modifica a propriedade de criptografia de dados transparente (TDE) de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8185e-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="8185e-107">Para obter mais informações, consulte criptografia de dados transparente com o banco de dados SQL do Azure https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) na biblioteca do Microsoft Developer Network).</span><span class="sxs-lookup"><span data-stu-id="8185e-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="8185e-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="8185e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8185e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8185e-109">EXAMPLES</span></span>

### <span data-ttu-id="8185e-110">Exemplo 1: habilitar o TDE para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="8185e-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="8185e-111">Esse comando habilita TDE para o banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="8185e-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="8185e-112">OS</span><span class="sxs-lookup"><span data-stu-id="8185e-112">PARAMETERS</span></span>

### <span data-ttu-id="8185e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8185e-113">-DatabaseName</span></span>
<span data-ttu-id="8185e-114">Especifica o nome do banco de dados que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8185e-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8185e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8185e-115">-DefaultProfile</span></span>
<span data-ttu-id="8185e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8185e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8185e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8185e-117">-ResourceGroupName</span></span>
<span data-ttu-id="8185e-118">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="8185e-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8185e-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="8185e-119">-ServerName</span></span>
<span data-ttu-id="8185e-120">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8185e-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="8185e-121">-Estado</span><span class="sxs-lookup"><span data-stu-id="8185e-121">-State</span></span>
<span data-ttu-id="8185e-122">Especifica o valor da propriedade TDE.</span><span class="sxs-lookup"><span data-stu-id="8185e-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="8185e-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8185e-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8185e-124">Possibilita</span><span class="sxs-lookup"><span data-stu-id="8185e-124">Enabled</span></span> 
- <span data-ttu-id="8185e-125">Ativo</span><span class="sxs-lookup"><span data-stu-id="8185e-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8185e-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8185e-126">-Confirm</span></span>
<span data-ttu-id="8185e-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8185e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8185e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8185e-128">-WhatIf</span></span>
<span data-ttu-id="8185e-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8185e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8185e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8185e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8185e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8185e-131">CommonParameters</span></span>
<span data-ttu-id="8185e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8185e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8185e-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8185e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8185e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8185e-134">INPUTS</span></span>

### <span data-ttu-id="8185e-135">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="8185e-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="8185e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8185e-136">System.String</span></span>

## <span data-ttu-id="8185e-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8185e-137">OUTPUTS</span></span>

### <span data-ttu-id="8185e-138">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="8185e-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="8185e-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8185e-139">NOTES</span></span>

## <span data-ttu-id="8185e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8185e-140">RELATED LINKS</span></span>

[<span data-ttu-id="8185e-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="8185e-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="8185e-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="8185e-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="8185e-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="8185e-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


