---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: d20e6f838370e73dc4d6ff849e6088df9b9f28cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432880"
---
# <span data-ttu-id="16e45-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="16e45-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="16e45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16e45-102">SYNOPSIS</span></span>
<span data-ttu-id="16e45-103">Remove uma regra de máscara de dados de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="16e45-103">Removes a data masking rule from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16e45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16e45-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e45-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16e45-105">DESCRIPTION</span></span>
<span data-ttu-id="16e45-106">O cmdlet **Remove-AzureRmSqlDatabaseDataMaskingRule** remove uma regra de máscara de dados específica de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="16e45-106">The **Remove-AzureRmSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="16e45-107">Você pode remover uma regra de máscara de dados usando os parâmetros *ResourceGroupName* , *nome_do_servidor* , *DatabaseName* e *RuleId* para identificar a regra que esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="16e45-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>

<span data-ttu-id="16e45-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="16e45-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="16e45-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16e45-109">EXAMPLES</span></span>

### <span data-ttu-id="16e45-110">Exemplo 1: remover uma regra de máscara de dados de banco de dados</span><span class="sxs-lookup"><span data-stu-id="16e45-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="16e45-111">Esse comando Remove o nome da regra Rule01 definido para o banco de dados Database01.</span><span class="sxs-lookup"><span data-stu-id="16e45-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="16e45-112">O banco de dados está localizado no Server01 e atribuído à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16e45-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="16e45-113">OS</span><span class="sxs-lookup"><span data-stu-id="16e45-113">PARAMETERS</span></span>

### <span data-ttu-id="16e45-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="16e45-114">-ColumnName</span></span>
<span data-ttu-id="16e45-115">Especifica o nome da coluna direcionada pela regra de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="16e45-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16e45-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16e45-116">-DatabaseName</span></span>
<span data-ttu-id="16e45-117">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="16e45-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="16e45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e45-118">-DefaultProfile</span></span>
<span data-ttu-id="16e45-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="16e45-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16e45-120">-Force</span><span class="sxs-lookup"><span data-stu-id="16e45-120">-Force</span></span>
<span data-ttu-id="16e45-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="16e45-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e45-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16e45-122">-PassThru</span></span>
<span data-ttu-id="16e45-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="16e45-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="16e45-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="16e45-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e45-125">-ResourceGroupName</span></span>
<span data-ttu-id="16e45-126">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="16e45-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="16e45-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="16e45-127">-SchemaName</span></span>
<span data-ttu-id="16e45-128">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="16e45-128">Specifies the name of a schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16e45-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="16e45-129">-ServerName</span></span>
<span data-ttu-id="16e45-130">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="16e45-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="16e45-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="16e45-131">-TableName</span></span>
<span data-ttu-id="16e45-132">Especifica o nome de uma tabela SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="16e45-132">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16e45-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16e45-133">-Confirm</span></span>
<span data-ttu-id="16e45-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16e45-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e45-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e45-135">-WhatIf</span></span>
<span data-ttu-id="16e45-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16e45-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e45-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16e45-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e45-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e45-138">CommonParameters</span></span>
<span data-ttu-id="16e45-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e45-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e45-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e45-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e45-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16e45-141">INPUTS</span></span>

### <span data-ttu-id="16e45-142">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="16e45-142">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="16e45-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16e45-143">OUTPUTS</span></span>

### <span data-ttu-id="16e45-144">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="16e45-144">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="16e45-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16e45-145">NOTES</span></span>

## <span data-ttu-id="16e45-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16e45-146">RELATED LINKS</span></span>

[<span data-ttu-id="16e45-147">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="16e45-147">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="16e45-148">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="16e45-148">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="16e45-149">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="16e45-149">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="16e45-150">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="16e45-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


