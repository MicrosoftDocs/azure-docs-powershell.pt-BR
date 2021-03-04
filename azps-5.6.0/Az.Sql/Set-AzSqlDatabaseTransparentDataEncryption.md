---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 8e511fa2e83866ac1a0119c410369f7f13705f14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892025"
---
# <span data-ttu-id="78d8e-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="78d8e-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="78d8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="78d8e-103">Modifica a propriedade TDE para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="78d8e-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="78d8e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="78d8e-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d8e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="78d8e-105">DESCRIPTION</span></span>
<span data-ttu-id="78d8e-106">O cmdlet **Set-AzSqlDatabaseTransparentDataEncryption** modifica a propriedade TDE (Criptografia de Dados Transparentes) de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="78d8e-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="78d8e-107">Para obter mais informações, consulte Transparent Data Encryption with Azure SQL Database https://msdn.microsoft.com/library/dn948096 ( in the Microsoft Developer Network https://msdn.microsoft.com/library/dn948096) Library.</span><span class="sxs-lookup"><span data-stu-id="78d8e-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="78d8e-108">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="78d8e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="78d8e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78d8e-109">EXAMPLES</span></span>

### <span data-ttu-id="78d8e-110">Exemplo 1: Habilitar o TDE para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="78d8e-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="78d8e-111">Esse comando habilita o TDE para o banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="78d8e-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="78d8e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="78d8e-112">PARAMETERS</span></span>

### <span data-ttu-id="78d8e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78d8e-113">-DatabaseName</span></span>
<span data-ttu-id="78d8e-114">Especifica o nome do banco de dados que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="78d8e-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="78d8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d8e-115">-DefaultProfile</span></span>
<span data-ttu-id="78d8e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="78d8e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78d8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="78d8e-118">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="78d8e-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="78d8e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="78d8e-119">-ServerName</span></span>
<span data-ttu-id="78d8e-120">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="78d8e-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="78d8e-121">-State</span><span class="sxs-lookup"><span data-stu-id="78d8e-121">-State</span></span>
<span data-ttu-id="78d8e-122">Especifica o valor da propriedade TDE.</span><span class="sxs-lookup"><span data-stu-id="78d8e-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="78d8e-123">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="78d8e-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="78d8e-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="78d8e-124">Enabled</span></span> 
- <span data-ttu-id="78d8e-125">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="78d8e-125">Disabled</span></span>

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

### <span data-ttu-id="78d8e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78d8e-126">-Confirm</span></span>
<span data-ttu-id="78d8e-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d8e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d8e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d8e-128">-WhatIf</span></span>
<span data-ttu-id="78d8e-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78d8e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d8e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78d8e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d8e-131">CommonParameters</span></span>
<span data-ttu-id="78d8e-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d8e-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78d8e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d8e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78d8e-134">INPUTS</span></span>

### <span data-ttu-id="78d8e-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="78d8e-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="78d8e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="78d8e-136">System.String</span></span>

## <span data-ttu-id="78d8e-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="78d8e-137">OUTPUTS</span></span>

### <span data-ttu-id="78d8e-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="78d8e-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="78d8e-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="78d8e-139">NOTES</span></span>

## <span data-ttu-id="78d8e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78d8e-140">RELATED LINKS</span></span>

[<span data-ttu-id="78d8e-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="78d8e-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="78d8e-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="78d8e-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="78d8e-143">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="78d8e-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


