---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 4e5f2578d0e9dbb2139b330ec0a7c2fe81b3124e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428029"
---
# <span data-ttu-id="993a6-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="993a6-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="993a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="993a6-102">SYNOPSIS</span></span>
<span data-ttu-id="993a6-103">Define as propriedades de uma regra de máscara de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="993a6-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="993a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="993a6-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="993a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="993a6-105">DESCRIPTION</span></span>
<span data-ttu-id="993a6-106">O cmdlet **set-AzureRmSqlDatabaseDataMaskingRule** define uma regra de máscara de dados para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="993a6-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="993a6-107">Para usar o cmdlet, forneça os parâmetros *ResourceGroupName* , *nome_do_servidor* , *DatabaseName* e *RuleId* para identificar a regra.</span><span class="sxs-lookup"><span data-stu-id="993a6-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="993a6-108">Você pode fornecer qualquer um dos parâmetros de *SchemaName* , *TableName* e *ColumnName* para redirecionar a regra.</span><span class="sxs-lookup"><span data-stu-id="993a6-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="993a6-109">Especifique o parâmetro *MaskingFunction* para modificar como os dados são mascarados.</span><span class="sxs-lookup"><span data-stu-id="993a6-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="993a6-110">Se você especificar um valor de número ou texto para *MaskingFunction* , poderá especificar os parâmetros *NumberFrom* e *numberto* para o mascaramento de número ou os parâmetros *PrefixSize* , *replaceString* e *SuffixSize* para o mascaramento de texto.</span><span class="sxs-lookup"><span data-stu-id="993a6-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="993a6-111">Se o comando for bem-sucedido e se você especificar o parâmetro *PassThru* , o cmdlet retornará um objeto que descreve as propriedades da regra de máscara de dados e os identificadores de regra.</span><span class="sxs-lookup"><span data-stu-id="993a6-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="993a6-112">Os identificadores de regra incluem, entre outros, **ResourceGroupName** , **nome_do_servidor** , **DatabaseName** e **RuleId**.</span><span class="sxs-lookup"><span data-stu-id="993a6-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="993a6-113">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="993a6-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="993a6-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="993a6-114">EXAMPLES</span></span>

### <span data-ttu-id="993a6-115">Exemplo 1: alterar o intervalo de uma regra de máscara de dados em um banco de dados</span><span class="sxs-lookup"><span data-stu-id="993a6-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="993a6-116">Esse comando modifica uma regra de máscara de dados que tem a ID Rule17.</span><span class="sxs-lookup"><span data-stu-id="993a6-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="993a6-117">Essa regra opera no banco de dados chamado Database01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="993a6-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="993a6-118">Esse comando altera os limites do intervalo no qual um número aleatório é gerado como o valor mascarado.</span><span class="sxs-lookup"><span data-stu-id="993a6-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="993a6-119">O novo intervalo está entre 23 e 42.</span><span class="sxs-lookup"><span data-stu-id="993a6-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="993a6-120">OS</span><span class="sxs-lookup"><span data-stu-id="993a6-120">PARAMETERS</span></span>

### <span data-ttu-id="993a6-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="993a6-121">-ColumnName</span></span>
<span data-ttu-id="993a6-122">Especifica o nome da coluna direcionada pela regra de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="993a6-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="993a6-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="993a6-123">-DatabaseName</span></span>
<span data-ttu-id="993a6-124">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="993a6-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="993a6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="993a6-125">-DefaultProfile</span></span>
<span data-ttu-id="993a6-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="993a6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="993a6-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="993a6-127">-MaskingFunction</span></span>
<span data-ttu-id="993a6-128">Especifica a função de mascaramento que a regra usa.</span><span class="sxs-lookup"><span data-stu-id="993a6-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="993a6-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="993a6-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="993a6-130">Assume</span><span class="sxs-lookup"><span data-stu-id="993a6-130">Default</span></span>
- <span data-ttu-id="993a6-131">Sem máscara</span><span class="sxs-lookup"><span data-stu-id="993a6-131">NoMasking</span></span>
- <span data-ttu-id="993a6-132">Textos</span><span class="sxs-lookup"><span data-stu-id="993a6-132">Text</span></span>
- <span data-ttu-id="993a6-133">Tempo</span><span class="sxs-lookup"><span data-stu-id="993a6-133">Number</span></span>
- <span data-ttu-id="993a6-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="993a6-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="993a6-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="993a6-135">CreditCardNumber</span></span>
- <span data-ttu-id="993a6-136">E-mail o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="993a6-136">Email The default value is Default.</span></span>

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

### <span data-ttu-id="993a6-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="993a6-137">-NumberFrom</span></span>
<span data-ttu-id="993a6-138">Especifica o número limite inferior do intervalo no qual um valor aleatório é selecionado.</span><span class="sxs-lookup"><span data-stu-id="993a6-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="993a6-139">Especifique esse parâmetro somente se você especificar um valor de número para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="993a6-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="993a6-140">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="993a6-140">The default value is 0.</span></span>

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

### <span data-ttu-id="993a6-141">-Numberto</span><span class="sxs-lookup"><span data-stu-id="993a6-141">-NumberTo</span></span>
<span data-ttu-id="993a6-142">Especifica o número de limite superior do intervalo no qual um valor aleatório é selecionado.</span><span class="sxs-lookup"><span data-stu-id="993a6-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="993a6-143">Especifique esse parâmetro somente se você especificar um valor de número para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="993a6-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="993a6-144">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="993a6-144">The default value is 0.</span></span>

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

### <span data-ttu-id="993a6-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="993a6-145">-PassThru</span></span>
<span data-ttu-id="993a6-146">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="993a6-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="993a6-147">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="993a6-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="993a6-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="993a6-148">-PrefixSize</span></span>
<span data-ttu-id="993a6-149">Especifica o número de caracteres no início do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="993a6-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="993a6-150">Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="993a6-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="993a6-151">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="993a6-151">The default value is 0.</span></span>

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

### <span data-ttu-id="993a6-152">-Substitutostring</span><span class="sxs-lookup"><span data-stu-id="993a6-152">-ReplacementString</span></span>
<span data-ttu-id="993a6-153">Especifica o número de caracteres no final do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="993a6-153">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="993a6-154">Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="993a6-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="993a6-155">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="993a6-155">The default value is 0.</span></span>

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

### <span data-ttu-id="993a6-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="993a6-156">-ResourceGroupName</span></span>
<span data-ttu-id="993a6-157">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="993a6-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="993a6-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="993a6-158">-SchemaName</span></span>
<span data-ttu-id="993a6-159">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="993a6-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="993a6-160">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="993a6-160">-ServerName</span></span>
<span data-ttu-id="993a6-161">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="993a6-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="993a6-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="993a6-162">-SuffixSize</span></span>
<span data-ttu-id="993a6-163">Especifica o número de caracteres no final do texto que não estão mascarados.</span><span class="sxs-lookup"><span data-stu-id="993a6-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="993a6-164">Especifique esse parâmetro somente se você especificar um valor de texto para o parâmetro *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="993a6-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="993a6-165">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="993a6-165">The default value is 0.</span></span>

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

### <span data-ttu-id="993a6-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="993a6-166">-TableName</span></span>
<span data-ttu-id="993a6-167">Especifica o nome da tabela de banco de dados que contém a coluna mascarada.</span><span class="sxs-lookup"><span data-stu-id="993a6-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="993a6-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="993a6-168">-Confirm</span></span>
<span data-ttu-id="993a6-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="993a6-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="993a6-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="993a6-170">-WhatIf</span></span>
<span data-ttu-id="993a6-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="993a6-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="993a6-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="993a6-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="993a6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993a6-173">CommonParameters</span></span>
<span data-ttu-id="993a6-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="993a6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993a6-175">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="993a6-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993a6-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="993a6-176">INPUTS</span></span>

### <span data-ttu-id="993a6-177">System. String</span><span class="sxs-lookup"><span data-stu-id="993a6-177">System.String</span></span>

### <span data-ttu-id="993a6-178">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="993a6-178">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="993a6-179">System. Nullable ' 1 [[System. Double, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="993a6-179">System.Nullable\`1[[System.Double, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="993a6-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="993a6-180">OUTPUTS</span></span>

### <span data-ttu-id="993a6-181">Microsoft. Azure. Commands. Sql. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="993a6-181">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="993a6-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="993a6-182">NOTES</span></span>

## <span data-ttu-id="993a6-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="993a6-183">RELATED LINKS</span></span>

[<span data-ttu-id="993a6-184">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="993a6-184">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="993a6-185">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="993a6-185">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="993a6-186">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="993a6-186">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="993a6-187">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="993a6-187">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


