---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: f2e9cc38faab0af87eb20b3a60d61ab679c435d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111305"
---
# <span data-ttu-id="d8c44-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d8c44-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="d8c44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8c44-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c44-103">Modifica a propriedade TDE de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d8c44-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="d8c44-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8c44-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8c44-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8c44-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c44-106">O cmdlet **Set-AzSqlDatabaseTransparentDataEncryption** modifica a propriedade TDE (Criptografia de Dados Transparentes) de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8c44-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="d8c44-107">Para obter mais informações, consulte Criptografia de Dados Transparentes com o Banco de Dados SQL do Azure https://msdn.microsoft.com/library/dn948096 ( na Biblioteca de Rede do Desenvolvedor da https://msdn.microsoft.com/library/dn948096) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d8c44-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="d8c44-108">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="d8c44-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d8c44-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8c44-109">EXAMPLES</span></span>

### <span data-ttu-id="d8c44-110">Exemplo 1: Habilitar TDE para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="d8c44-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="d8c44-111">Esse comando habilita o TDE para o banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="d8c44-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="d8c44-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8c44-112">PARAMETERS</span></span>

### <span data-ttu-id="d8c44-113">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="d8c44-113">-DatabaseName</span></span>
<span data-ttu-id="d8c44-114">Especifica o nome do banco de dados que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d8c44-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d8c44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c44-115">-DefaultProfile</span></span>
<span data-ttu-id="d8c44-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d8c44-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8c44-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c44-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8c44-118">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="d8c44-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d8c44-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8c44-119">-ServerName</span></span>
<span data-ttu-id="d8c44-120">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d8c44-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d8c44-121">-Estado</span><span class="sxs-lookup"><span data-stu-id="d8c44-121">-State</span></span>
<span data-ttu-id="d8c44-122">Especifica o valor da propriedade TDE.</span><span class="sxs-lookup"><span data-stu-id="d8c44-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="d8c44-123">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d8c44-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8c44-124">Habilitado</span><span class="sxs-lookup"><span data-stu-id="d8c44-124">Enabled</span></span> 
- <span data-ttu-id="d8c44-125">Desativado</span><span class="sxs-lookup"><span data-stu-id="d8c44-125">Disabled</span></span>

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

### <span data-ttu-id="d8c44-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d8c44-126">-Confirm</span></span>
<span data-ttu-id="d8c44-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8c44-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c44-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c44-128">-WhatIf</span></span>
<span data-ttu-id="d8c44-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d8c44-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8c44-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8c44-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8c44-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c44-131">CommonParameters</span></span>
<span data-ttu-id="d8c44-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c44-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c44-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8c44-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c44-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="d8c44-134">INPUTS</span></span>

### <span data-ttu-id="d8c44-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="d8c44-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="d8c44-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d8c44-136">System.String</span></span>

## <span data-ttu-id="d8c44-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="d8c44-137">OUTPUTS</span></span>

### <span data-ttu-id="d8c44-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="d8c44-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="d8c44-139">Notas</span><span class="sxs-lookup"><span data-stu-id="d8c44-139">NOTES</span></span>

## <span data-ttu-id="d8c44-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8c44-140">RELATED LINKS</span></span>

[<span data-ttu-id="d8c44-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="d8c44-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="d8c44-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="d8c44-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="d8c44-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d8c44-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


