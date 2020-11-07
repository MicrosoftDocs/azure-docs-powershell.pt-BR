---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: eb5e809b3f48403a6095f84643af0a169b2cecf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773851"
---
# <span data-ttu-id="35e6b-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="35e6b-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="35e6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="35e6b-103">Cria uma regra de máscara de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35e6b-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="35e6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35e6b-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35e6b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="35e6b-106">O cmdlet **New-AzSqlDatabaseDataMaskingRule** cria uma regra de máscara de dados para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="35e6b-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="35e6b-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *nome_do_servidor* , *DatabaseName* e *RuleId* para identificar a regra.</span><span class="sxs-lookup"><span data-stu-id="35e6b-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="35e6b-108">Forneça a *TableName* e *ColumnName* para especificar o destino da regra e o parâmetro *MaskingFunction* para definir como os dados são mascarados.</span><span class="sxs-lookup"><span data-stu-id="35e6b-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="35e6b-109">Se *MaskingFunction* tiver um valor de número ou texto, você poderá especificar os parâmetros *NumberFrom* e *numberto* , para o mascaramento de números ou o *PrefixSize* , o *replaceString* e o *SuffixSize* para o mascaramento de texto.</span><span class="sxs-lookup"><span data-stu-id="35e6b-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="35e6b-110">Se o comando for bem-sucedido e o parâmetro *PassThru* for usado, o cmdlet retornará um objeto que descreve as propriedades da regra de máscara de dados, além dos identificadores de regra.</span><span class="sxs-lookup"><span data-stu-id="35e6b-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="35e6b-111">Os identificadores de regra incluem, entre outros, *ResourceGroupName* , *nome_do_servidor* , *DatabaseName* e *RuleId*.</span><span class="sxs-lookup"><span data-stu-id="35e6b-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>
<span data-ttu-id="35e6b-112">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="35e6b-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="35e6b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35e6b-113">EXAMPLES</span></span>

### <span data-ttu-id="35e6b-114">Exemplo 1: criar uma regra de máscara de dados para uma coluna de número em um banco de dados</span><span class="sxs-lookup"><span data-stu-id="35e6b-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="35e6b-115">Esse comando cria uma regra de máscara de dados para a coluna chamada Column01 na tabela denominada Table01 no esquema chamado Schema01.</span><span class="sxs-lookup"><span data-stu-id="35e6b-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="35e6b-116">O banco de dados chamado Database01 contém todos esses itens.</span><span class="sxs-lookup"><span data-stu-id="35e6b-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="35e6b-117">A regra é uma regra de mascaramento de número que usa um número aleatório entre 5 e 14 como o valor de máscara.</span><span class="sxs-lookup"><span data-stu-id="35e6b-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="35e6b-118">A regra se chama Rule01.</span><span class="sxs-lookup"><span data-stu-id="35e6b-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="35e6b-119">OS</span><span class="sxs-lookup"><span data-stu-id="35e6b-119">PARAMETERS</span></span>

### <span data-ttu-id="35e6b-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="35e6b-120">-ColumnName</span></span>
<span data-ttu-id="35e6b-121">Especifica o nome da coluna direcionada pela regra de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="35e6b-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="35e6b-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35e6b-122">-DatabaseName</span></span>
<span data-ttu-id="35e6b-123">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35e6b-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="35e6b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e6b-124">-DefaultProfile</span></span>
<span data-ttu-id="35e6b-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="35e6b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35e6b-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="35e6b-126">-MaskingFunction</span></span>
<span data-ttu-id="35e6b-127">Especifica a função de mascaramento que a regra usa.</span><span class="sxs-lookup"><span data-stu-id="35e6b-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="35e6b-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35e6b-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35e6b-129">Assume</span><span class="sxs-lookup"><span data-stu-id="35e6b-129">Default</span></span>
- <span data-ttu-id="35e6b-130">Sem máscara</span><span class="sxs-lookup"><span data-stu-id="35e6b-130">NoMasking</span></span>
- <span data-ttu-id="35e6b-131">Textos</span><span class="sxs-lookup"><span data-stu-id="35e6b-131">Text</span></span>
- <span data-ttu-id="35e6b-132">Tempo</span><span class="sxs-lookup"><span data-stu-id="35e6b-132">Number</span></span>
- <span data-ttu-id="35e6b-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="35e6b-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="35e6b-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="35e6b-134">CreditCardNumber</span></span>
- <span data-ttu-id="35e6b-135">E-mail o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="35e6b-135">Email The default value is Default.</span></span>

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

### <span data-ttu-id="35e6b-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="35e6b-136">-NumberFrom</span></span>
<span data-ttu-id="35e6b-137">Especifica o número limite inferior do intervalo no qual um valor aleatório é selecionado.</span><span class="sxs-lookup"><span data-stu-id="35e6b-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="35e6b-138">Especifique esse parâmetro somente se você especificar um valor de número para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="35e6b-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="35e6b-139">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="35e6b-139">The default value is 0.</span></span>

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

### <span data-ttu-id="35e6b-140">-Numberto</span><span class="sxs-lookup"><span data-stu-id="35e6b-140">-NumberTo</span></span>
<span data-ttu-id="35e6b-141">Especifica o número de limite superior do intervalo no qual um valor aleatório é selecionado.</span><span class="sxs-lookup"><span data-stu-id="35e6b-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="35e6b-142">Especifique esse parâmetro somente se você especificar um valor de número para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="35e6b-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="35e6b-143">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="35e6b-143">The default value is 0.</span></span>

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

### <span data-ttu-id="35e6b-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35e6b-144">-PassThru</span></span>
<span data-ttu-id="35e6b-145">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="35e6b-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="35e6b-146">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="35e6b-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35e6b-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="35e6b-147">-PrefixSize</span></span>
<span data-ttu-id="35e6b-148">Especifica o número de caracteres no início do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="35e6b-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="35e6b-149">Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="35e6b-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="35e6b-150">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="35e6b-150">The default value is 0.</span></span>

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

### <span data-ttu-id="35e6b-151">-Substitutostring</span><span class="sxs-lookup"><span data-stu-id="35e6b-151">-ReplacementString</span></span>
<span data-ttu-id="35e6b-152">Especifica o número de caracteres no final do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="35e6b-152">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="35e6b-153">Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="35e6b-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="35e6b-154">O valor padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="35e6b-154">The default value is an empty string.</span></span>

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

### <span data-ttu-id="35e6b-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e6b-155">-ResourceGroupName</span></span>
<span data-ttu-id="35e6b-156">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="35e6b-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="35e6b-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="35e6b-157">-SchemaName</span></span>
<span data-ttu-id="35e6b-158">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="35e6b-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="35e6b-159">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="35e6b-159">-ServerName</span></span>
<span data-ttu-id="35e6b-160">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35e6b-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="35e6b-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="35e6b-161">-SuffixSize</span></span>
<span data-ttu-id="35e6b-162">Especifica o número de caracteres no final do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="35e6b-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="35e6b-163">Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="35e6b-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="35e6b-164">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="35e6b-164">The default value is 0.</span></span>

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

### <span data-ttu-id="35e6b-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="35e6b-165">-TableName</span></span>
<span data-ttu-id="35e6b-166">Especifica o nome da tabela de banco de dados que contém a coluna mascarada.</span><span class="sxs-lookup"><span data-stu-id="35e6b-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="35e6b-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35e6b-167">-Confirm</span></span>
<span data-ttu-id="35e6b-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35e6b-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35e6b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e6b-169">-WhatIf</span></span>
<span data-ttu-id="35e6b-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35e6b-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35e6b-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35e6b-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35e6b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e6b-172">CommonParameters</span></span>
<span data-ttu-id="35e6b-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e6b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e6b-174">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35e6b-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e6b-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35e6b-175">INPUTS</span></span>

### <span data-ttu-id="35e6b-176">System. String</span><span class="sxs-lookup"><span data-stu-id="35e6b-176">System.String</span></span>

### <span data-ttu-id="35e6b-177">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="35e6b-177">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="35e6b-178">System. Nullable ' 1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="35e6b-178">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="35e6b-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35e6b-179">OUTPUTS</span></span>

### <span data-ttu-id="35e6b-180">Microsoft. Azure. Commands. Sql. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="35e6b-180">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="35e6b-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35e6b-181">NOTES</span></span>

## <span data-ttu-id="35e6b-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35e6b-182">RELATED LINKS</span></span>

[<span data-ttu-id="35e6b-183">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="35e6b-183">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="35e6b-184">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="35e6b-184">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="35e6b-185">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="35e6b-185">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="35e6b-186">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="35e6b-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


