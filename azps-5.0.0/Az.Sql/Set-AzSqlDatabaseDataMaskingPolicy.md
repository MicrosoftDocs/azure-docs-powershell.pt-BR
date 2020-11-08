---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124740"
---
# <span data-ttu-id="9891f-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="9891f-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="9891f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9891f-102">SYNOPSIS</span></span>
<span data-ttu-id="9891f-103">Define o mascaramento de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9891f-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="9891f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9891f-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9891f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9891f-105">DESCRIPTION</span></span>
<span data-ttu-id="9891f-106">O cmdlet **set-AzSqlDatabaseDataMaskingPolicy** define a política de máscara de dados de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="9891f-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="9891f-107">Para usar esse cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9891f-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="9891f-108">Você pode definir o parâmetro *DataMaskingState* para especificar se as operações de máscara de dados estão habilitadas ou desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="9891f-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="9891f-109">Se o cmdlet for bem-sucedido e o parâmetro *PassThru* for usado, ele retornará um objeto que descreve a política de mascaramento de dados atual, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9891f-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="9891f-110">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="9891f-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="9891f-111">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="9891f-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9891f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9891f-112">EXAMPLES</span></span>

### <span data-ttu-id="9891f-113">Exemplo 1: definir a política de máscara de dados para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="9891f-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="9891f-114">Esse comando define a política de máscara de dados para um banco de dados denominado database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="9891f-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="9891f-115">OS</span><span class="sxs-lookup"><span data-stu-id="9891f-115">PARAMETERS</span></span>

### <span data-ttu-id="9891f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9891f-116">-DatabaseName</span></span>
<span data-ttu-id="9891f-117">Especifica o nome do banco de dados onde a política está definida.</span><span class="sxs-lookup"><span data-stu-id="9891f-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="9891f-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="9891f-118">-DataMaskingState</span></span>
<span data-ttu-id="9891f-119">Especifica se a operação de máscara de dados está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="9891f-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="9891f-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9891f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9891f-121">Possibilita</span><span class="sxs-lookup"><span data-stu-id="9891f-121">Enabled</span></span>
- <span data-ttu-id="9891f-122">Desativado o valor padrão é habilitado.</span><span class="sxs-lookup"><span data-stu-id="9891f-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9891f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9891f-123">-DefaultProfile</span></span>
<span data-ttu-id="9891f-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9891f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9891f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9891f-125">-PassThru</span></span>
<span data-ttu-id="9891f-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9891f-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9891f-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9891f-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9891f-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="9891f-128">-PrivilegedUsers</span></span>
<span data-ttu-id="9891f-129">Especifica uma lista separada por ponto-e-vírgula de IDs de usuário privilegiadas.</span><span class="sxs-lookup"><span data-stu-id="9891f-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="9891f-130">Esses usuários têm permissão para exibir os dados de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="9891f-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="9891f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9891f-131">-ResourceGroupName</span></span>
<span data-ttu-id="9891f-132">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="9891f-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9891f-133">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="9891f-133">-ServerName</span></span>
<span data-ttu-id="9891f-134">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9891f-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="9891f-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9891f-135">-Confirm</span></span>
<span data-ttu-id="9891f-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9891f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9891f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9891f-137">-WhatIf</span></span>
<span data-ttu-id="9891f-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9891f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9891f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9891f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9891f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9891f-140">CommonParameters</span></span>
<span data-ttu-id="9891f-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9891f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9891f-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9891f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9891f-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9891f-143">INPUTS</span></span>

### <span data-ttu-id="9891f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9891f-144">System.String</span></span>

## <span data-ttu-id="9891f-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9891f-145">OUTPUTS</span></span>

### <span data-ttu-id="9891f-146">Microsoft. Azure. Commands. Sql. datamasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9891f-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="9891f-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9891f-147">NOTES</span></span>

## <span data-ttu-id="9891f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9891f-148">RELATED LINKS</span></span>

[<span data-ttu-id="9891f-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="9891f-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="9891f-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9891f-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9891f-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9891f-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9891f-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9891f-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9891f-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9891f-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9891f-154">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="9891f-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


