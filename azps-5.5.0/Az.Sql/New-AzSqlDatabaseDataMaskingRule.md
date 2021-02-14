---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111323"
---
# <span data-ttu-id="c15fd-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c15fd-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="c15fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c15fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c15fd-103">Cria uma regra de mascaramento de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c15fd-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="c15fd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c15fd-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c15fd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c15fd-105">DESCRIPTION</span></span>
<span data-ttu-id="c15fd-106">O cmdlet **New-AzSqlDatabaseDataMaskingRule** cria uma regra de mascaramento de dados para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c15fd-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="c15fd-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName,* *ServerName* e *DatabaseName* para identificar a regra.</span><span class="sxs-lookup"><span data-stu-id="c15fd-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="c15fd-108">Forneça o *NomeDa Table e* *o NomeDa* Coluna para especificar o destino da regra e o parâmetro *MascararFunção* para definir como os dados são máscaras.</span><span class="sxs-lookup"><span data-stu-id="c15fd-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="c15fd-109">Se a Função *Mascarar* tiver um valor de Número ou Texto, você poderá especificar os parâmetros *NumberFrom* e *NumberTo,* para mascaramento de número, ou *PrefixSize,* *ReplacementString* e *SufixoSize* para mascaramento de texto.</span><span class="sxs-lookup"><span data-stu-id="c15fd-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize*, *ReplacementString*, and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="c15fd-110">Se o comando for bem-sucedido e o parâmetro *PassThru* for usado, o cmdlet retornará um objeto que descreve as propriedades da regra de mascaramento de dados além dos identificadores de regra.</span><span class="sxs-lookup"><span data-stu-id="c15fd-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="c15fd-111">Os identificadores de regra incluem, mas não estão limitados a, *ResourceGroupName,* *ServerName,* *DatabaseName* e *RuleID.*</span><span class="sxs-lookup"><span data-stu-id="c15fd-111">Rule identifiers include, but are not limited to, *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleID*.</span></span>
<span data-ttu-id="c15fd-112">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="c15fd-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c15fd-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c15fd-113">EXAMPLES</span></span>

### <span data-ttu-id="c15fd-114">Exemplo 1: Criar uma regra de mascaramento de dados para uma coluna de número em um banco de dados</span><span class="sxs-lookup"><span data-stu-id="c15fd-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="c15fd-115">Esse comando cria uma regra de mascaramento de dados para a coluna chamada Coluna01 na tabela chamada Tabela01 no esquema denominado Esquema01.</span><span class="sxs-lookup"><span data-stu-id="c15fd-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="c15fd-116">O banco de dados chamado Database01 contém todos esses itens.</span><span class="sxs-lookup"><span data-stu-id="c15fd-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="c15fd-117">A regra é uma regra de mascaramento de número que usa um número aleatório entre 5 e 14 como o valor da máscara.</span><span class="sxs-lookup"><span data-stu-id="c15fd-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="c15fd-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c15fd-118">PARAMETERS</span></span>

### <span data-ttu-id="c15fd-119">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="c15fd-119">-ColumnName</span></span>
<span data-ttu-id="c15fd-120">Especifica o nome da coluna direcionada pela regra de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="c15fd-120">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15fd-121">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="c15fd-121">-DatabaseName</span></span>
<span data-ttu-id="c15fd-122">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c15fd-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="c15fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c15fd-123">-DefaultProfile</span></span>
<span data-ttu-id="c15fd-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c15fd-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c15fd-125">-MascararFunção</span><span class="sxs-lookup"><span data-stu-id="c15fd-125">-MaskingFunction</span></span>
<span data-ttu-id="c15fd-126">Especifica a função de mascaramento que a regra usa.</span><span class="sxs-lookup"><span data-stu-id="c15fd-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="c15fd-127">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c15fd-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c15fd-128">Padrão</span><span class="sxs-lookup"><span data-stu-id="c15fd-128">Default</span></span>
- <span data-ttu-id="c15fd-129">NoMasking</span><span class="sxs-lookup"><span data-stu-id="c15fd-129">NoMasking</span></span>
- <span data-ttu-id="c15fd-130">Texto</span><span class="sxs-lookup"><span data-stu-id="c15fd-130">Text</span></span>
- <span data-ttu-id="c15fd-131">Número</span><span class="sxs-lookup"><span data-stu-id="c15fd-131">Number</span></span>
- <span data-ttu-id="c15fd-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="c15fd-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="c15fd-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="c15fd-133">CreditCardNumber</span></span>
- <span data-ttu-id="c15fd-134">Email O valor padrão é Padrão.</span><span class="sxs-lookup"><span data-stu-id="c15fd-134">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15fd-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="c15fd-135">-NumberFrom</span></span>
<span data-ttu-id="c15fd-136">Especifica o número de limite inferior do intervalo a partir do qual um valor aleatório é selecionado.</span><span class="sxs-lookup"><span data-stu-id="c15fd-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="c15fd-137">Especifique esse parâmetro somente se você especificar um valor de Número para *o parâmetro MascaramentoFuncional.*</span><span class="sxs-lookup"><span data-stu-id="c15fd-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="c15fd-138">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="c15fd-138">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15fd-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="c15fd-139">-NumberTo</span></span>
<span data-ttu-id="c15fd-140">Especifica o número de limite superior do intervalo a partir do qual um valor aleatório é selecionado.</span><span class="sxs-lookup"><span data-stu-id="c15fd-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="c15fd-141">Especifique esse parâmetro somente se você especificar um valor de Número para *o parâmetro MascaramentoFuncional.*</span><span class="sxs-lookup"><span data-stu-id="c15fd-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="c15fd-142">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="c15fd-142">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15fd-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c15fd-143">-PassThru</span></span>
<span data-ttu-id="c15fd-144">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c15fd-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c15fd-145">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="c15fd-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c15fd-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="c15fd-146">-PrefixSize</span></span>
<span data-ttu-id="c15fd-147">Especifica o número de caracteres no início do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="c15fd-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="c15fd-148">Especifique esse parâmetro somente se você especificar um valor de Texto para *o parâmetro MascaramentoFuncional.*</span><span class="sxs-lookup"><span data-stu-id="c15fd-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="c15fd-149">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="c15fd-149">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15fd-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="c15fd-150">-ReplacementString</span></span>
<span data-ttu-id="c15fd-151">Especifica o número de caracteres no final do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="c15fd-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="c15fd-152">Especifique esse parâmetro somente se você especificar um valor de Texto para *o parâmetro MascaramentoFuncional.*</span><span class="sxs-lookup"><span data-stu-id="c15fd-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="c15fd-153">O valor padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="c15fd-153">The default value is an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15fd-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c15fd-154">-ResourceGroupName</span></span>
<span data-ttu-id="c15fd-155">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="c15fd-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c15fd-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c15fd-156">-SchemaName</span></span>
<span data-ttu-id="c15fd-157">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="c15fd-157">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15fd-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c15fd-158">-ServerName</span></span>
<span data-ttu-id="c15fd-159">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c15fd-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="c15fd-160">-SufixoSize</span><span class="sxs-lookup"><span data-stu-id="c15fd-160">-SuffixSize</span></span>
<span data-ttu-id="c15fd-161">Especifica o número de caracteres no final do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="c15fd-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="c15fd-162">Especifique esse parâmetro somente se você especificar um valor de Texto para *o parâmetro MascaramentoFuncional.*</span><span class="sxs-lookup"><span data-stu-id="c15fd-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="c15fd-163">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="c15fd-163">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15fd-164">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="c15fd-164">-TableName</span></span>
<span data-ttu-id="c15fd-165">Especifica o nome da tabela de banco de dados que contém a coluna mascarada.</span><span class="sxs-lookup"><span data-stu-id="c15fd-165">Specifies the name of the database table that contains the masked column.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15fd-166">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c15fd-166">-Confirm</span></span>
<span data-ttu-id="c15fd-167">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c15fd-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c15fd-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c15fd-168">-WhatIf</span></span>
<span data-ttu-id="c15fd-169">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c15fd-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c15fd-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c15fd-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c15fd-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15fd-171">CommonParameters</span></span>
<span data-ttu-id="c15fd-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c15fd-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15fd-173">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c15fd-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15fd-174">Entradas</span><span class="sxs-lookup"><span data-stu-id="c15fd-174">INPUTS</span></span>

### <span data-ttu-id="c15fd-175">System.String</span><span class="sxs-lookup"><span data-stu-id="c15fd-175">System.String</span></span>

### <span data-ttu-id="c15fd-176">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c15fd-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c15fd-177">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c15fd-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c15fd-178">Saídas</span><span class="sxs-lookup"><span data-stu-id="c15fd-178">OUTPUTS</span></span>

### <span data-ttu-id="c15fd-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="c15fd-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="c15fd-180">Notas</span><span class="sxs-lookup"><span data-stu-id="c15fd-180">NOTES</span></span>

## <span data-ttu-id="c15fd-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c15fd-181">RELATED LINKS</span></span>

[<span data-ttu-id="c15fd-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c15fd-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c15fd-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c15fd-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c15fd-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c15fd-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c15fd-185">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="c15fd-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


