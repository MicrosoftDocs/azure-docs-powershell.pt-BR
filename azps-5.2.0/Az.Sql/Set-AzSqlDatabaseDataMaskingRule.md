---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260115"
---
# <span data-ttu-id="e7eef-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e7eef-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="e7eef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7eef-102">SYNOPSIS</span></span>
<span data-ttu-id="e7eef-103">Define as propriedades de uma regra de máscara de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e7eef-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="e7eef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7eef-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7eef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7eef-105">DESCRIPTION</span></span>
<span data-ttu-id="e7eef-106">O cmdlet **set-AzSqlDatabaseDataMaskingRule** define uma regra de máscara de dados para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7eef-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="e7eef-107">Para usar o cmdlet, forneça os parâmetros *ResourceGroupName*, *nome_do_servidor*, *DatabaseName* e *RuleId* para identificar a regra.</span><span class="sxs-lookup"><span data-stu-id="e7eef-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="e7eef-108">Você pode fornecer qualquer um dos parâmetros de *SchemaName*, *TableName* e *ColumnName* para redirecionar a regra.</span><span class="sxs-lookup"><span data-stu-id="e7eef-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="e7eef-109">Especifique o parâmetro *MaskingFunction* para modificar como os dados são mascarados.</span><span class="sxs-lookup"><span data-stu-id="e7eef-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="e7eef-110">Se você especificar um valor de número ou texto para *MaskingFunction*, poderá especificar os parâmetros *NumberFrom* e *numberto* para o mascaramento de número ou os parâmetros *PrefixSize*, *replaceString* e *SuffixSize* para o mascaramento de texto.</span><span class="sxs-lookup"><span data-stu-id="e7eef-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="e7eef-111">Se o comando for bem-sucedido e se você especificar o parâmetro *PassThru* , o cmdlet retornará um objeto que descreve as propriedades da regra de máscara de dados e os identificadores de regra.</span><span class="sxs-lookup"><span data-stu-id="e7eef-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="e7eef-112">Os identificadores de regra incluem, entre outros, **ResourceGroupName**, **nome_do_servidor**, **DatabaseName** e **RuleId**.</span><span class="sxs-lookup"><span data-stu-id="e7eef-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="e7eef-113">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="e7eef-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e7eef-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7eef-114">EXAMPLES</span></span>

### <span data-ttu-id="e7eef-115">Exemplo 1: alterar o intervalo de uma regra de máscara de dados em um banco de dados</span><span class="sxs-lookup"><span data-stu-id="e7eef-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="e7eef-116">Esse comando modifica uma regra de máscara de dados que tem a ID Rule17.</span><span class="sxs-lookup"><span data-stu-id="e7eef-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="e7eef-117">Essa regra opera no banco de dados chamado Database01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="e7eef-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="e7eef-118">Esse comando altera os limites do intervalo no qual um número aleatório é gerado como o valor mascarado.</span><span class="sxs-lookup"><span data-stu-id="e7eef-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="e7eef-119">O novo intervalo está entre 23 e 42.</span><span class="sxs-lookup"><span data-stu-id="e7eef-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="e7eef-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e7eef-120">Example 2</span></span>

<span data-ttu-id="e7eef-121">Define as propriedades de uma regra de máscara de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e7eef-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="e7eef-122">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e7eef-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="e7eef-123">OS</span><span class="sxs-lookup"><span data-stu-id="e7eef-123">PARAMETERS</span></span>

### <span data-ttu-id="e7eef-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e7eef-124">-ColumnName</span></span>
<span data-ttu-id="e7eef-125">Especifica o nome da coluna direcionada pela regra de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="e7eef-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="e7eef-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7eef-126">-DatabaseName</span></span>
<span data-ttu-id="e7eef-127">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e7eef-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="e7eef-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7eef-128">-DefaultProfile</span></span>
<span data-ttu-id="e7eef-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e7eef-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7eef-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="e7eef-130">-MaskingFunction</span></span>
<span data-ttu-id="e7eef-131">Especifica a função de mascaramento que a regra usa.</span><span class="sxs-lookup"><span data-stu-id="e7eef-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="e7eef-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e7eef-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7eef-133">Assume</span><span class="sxs-lookup"><span data-stu-id="e7eef-133">Default</span></span>
- <span data-ttu-id="e7eef-134">Sem máscara</span><span class="sxs-lookup"><span data-stu-id="e7eef-134">NoMasking</span></span>
- <span data-ttu-id="e7eef-135">Textos</span><span class="sxs-lookup"><span data-stu-id="e7eef-135">Text</span></span>
- <span data-ttu-id="e7eef-136">Tempo</span><span class="sxs-lookup"><span data-stu-id="e7eef-136">Number</span></span>
- <span data-ttu-id="e7eef-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="e7eef-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="e7eef-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="e7eef-138">CreditCardNumber</span></span>
- <span data-ttu-id="e7eef-139">E-mail o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="e7eef-139">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7eef-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="e7eef-140">-NumberFrom</span></span>
<span data-ttu-id="e7eef-141">Especifica o número limite inferior do intervalo no qual um valor aleatório é selecionado.</span><span class="sxs-lookup"><span data-stu-id="e7eef-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="e7eef-142">Especifique esse parâmetro somente se você especificar um valor de número para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="e7eef-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="e7eef-143">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="e7eef-143">The default value is 0.</span></span>

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

### <span data-ttu-id="e7eef-144">-Numberto</span><span class="sxs-lookup"><span data-stu-id="e7eef-144">-NumberTo</span></span>
<span data-ttu-id="e7eef-145">Especifica o número de limite superior do intervalo no qual um valor aleatório é selecionado.</span><span class="sxs-lookup"><span data-stu-id="e7eef-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="e7eef-146">Especifique esse parâmetro somente se você especificar um valor de número para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="e7eef-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="e7eef-147">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="e7eef-147">The default value is 0.</span></span>

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

### <span data-ttu-id="e7eef-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7eef-148">-PassThru</span></span>
<span data-ttu-id="e7eef-149">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e7eef-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e7eef-150">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e7eef-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7eef-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="e7eef-151">-PrefixSize</span></span>
<span data-ttu-id="e7eef-152">Especifica o número de caracteres no início do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="e7eef-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="e7eef-153">Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="e7eef-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="e7eef-154">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="e7eef-154">The default value is 0.</span></span>

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

### <span data-ttu-id="e7eef-155">-Substitutostring</span><span class="sxs-lookup"><span data-stu-id="e7eef-155">-ReplacementString</span></span>
<span data-ttu-id="e7eef-156">Especifica o número de caracteres no final do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="e7eef-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="e7eef-157">Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="e7eef-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="e7eef-158">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="e7eef-158">The default value is 0.</span></span>

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

### <span data-ttu-id="e7eef-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7eef-159">-ResourceGroupName</span></span>
<span data-ttu-id="e7eef-160">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="e7eef-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e7eef-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e7eef-161">-SchemaName</span></span>
<span data-ttu-id="e7eef-162">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="e7eef-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="e7eef-163">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e7eef-163">-ServerName</span></span>
<span data-ttu-id="e7eef-164">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e7eef-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e7eef-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="e7eef-165">-SuffixSize</span></span>
<span data-ttu-id="e7eef-166">Especifica o número de caracteres no final do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="e7eef-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="e7eef-167">Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="e7eef-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="e7eef-168">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="e7eef-168">The default value is 0.</span></span>

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

### <span data-ttu-id="e7eef-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="e7eef-169">-TableName</span></span>
<span data-ttu-id="e7eef-170">Especifica o nome da tabela de banco de dados que contém a coluna mascarada.</span><span class="sxs-lookup"><span data-stu-id="e7eef-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="e7eef-171">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7eef-171">-Confirm</span></span>
<span data-ttu-id="e7eef-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7eef-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7eef-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7eef-173">-WhatIf</span></span>
<span data-ttu-id="e7eef-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7eef-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7eef-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7eef-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7eef-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7eef-176">CommonParameters</span></span>
<span data-ttu-id="e7eef-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7eef-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7eef-178">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7eef-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7eef-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7eef-179">INPUTS</span></span>

### <span data-ttu-id="e7eef-180">System. String</span><span class="sxs-lookup"><span data-stu-id="e7eef-180">System.String</span></span>

### <span data-ttu-id="e7eef-181">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e7eef-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e7eef-182">System. Nullable ' 1 [[System. Double, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e7eef-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e7eef-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7eef-183">OUTPUTS</span></span>

### <span data-ttu-id="e7eef-184">Microsoft. Azure. Commands. Sql. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="e7eef-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="e7eef-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7eef-185">NOTES</span></span>

## <span data-ttu-id="e7eef-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7eef-186">RELATED LINKS</span></span>

[<span data-ttu-id="e7eef-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e7eef-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e7eef-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e7eef-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e7eef-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e7eef-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e7eef-190">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e7eef-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


