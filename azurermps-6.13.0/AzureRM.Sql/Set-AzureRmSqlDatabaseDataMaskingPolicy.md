---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d59891980c11b90ee73275dbccb6a98b65c89613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428028"
---
# <span data-ttu-id="ae02e-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae02e-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="ae02e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae02e-102">SYNOPSIS</span></span>
<span data-ttu-id="ae02e-103">Define o mascaramento de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ae02e-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae02e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae02e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae02e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae02e-105">DESCRIPTION</span></span>
<span data-ttu-id="ae02e-106">O cmdlet **set-AzureRmSqlDatabaseDataMaskingPolicy** define a política de máscara de dados de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae02e-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="ae02e-107">Para usar esse cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ae02e-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ae02e-108">Você pode definir o parâmetro *DataMaskingState* para especificar se as operações de máscara de dados estão habilitadas ou desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="ae02e-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="ae02e-109">Você também pode definir o parâmetro *PrivilegedLogins* para especificar quais usuários têm permissão para ver os dados não mascarados.</span><span class="sxs-lookup"><span data-stu-id="ae02e-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="ae02e-110">Se o cmdlet for bem-sucedido e o parâmetro *PassThru* for usado, ele retornará um objeto que descreve a política de mascaramento de dados atual, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ae02e-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="ae02e-111">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="ae02e-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="ae02e-112">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="ae02e-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ae02e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae02e-113">EXAMPLES</span></span>

### <span data-ttu-id="ae02e-114">Exemplo 1: definir a política de máscara de dados para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="ae02e-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="ae02e-115">Esse comando define a política de máscara de dados para um banco de dados denominado database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="ae02e-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="ae02e-116">OS</span><span class="sxs-lookup"><span data-stu-id="ae02e-116">PARAMETERS</span></span>

### <span data-ttu-id="ae02e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae02e-117">-DatabaseName</span></span>
<span data-ttu-id="ae02e-118">Especifica o nome do banco de dados onde a política está definida.</span><span class="sxs-lookup"><span data-stu-id="ae02e-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="ae02e-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="ae02e-119">-DataMaskingState</span></span>
<span data-ttu-id="ae02e-120">Especifica se a operação de máscara de dados está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="ae02e-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="ae02e-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ae02e-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ae02e-122">Possibilita</span><span class="sxs-lookup"><span data-stu-id="ae02e-122">Enabled</span></span>
- <span data-ttu-id="ae02e-123">Desativado o valor padrão é habilitado.</span><span class="sxs-lookup"><span data-stu-id="ae02e-123">Disabled The default value is Enabled.</span></span>

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

### <span data-ttu-id="ae02e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae02e-124">-DefaultProfile</span></span>
<span data-ttu-id="ae02e-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ae02e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae02e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae02e-126">-PassThru</span></span>
<span data-ttu-id="ae02e-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ae02e-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ae02e-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ae02e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae02e-129">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="ae02e-129">-PrivilegedLogins</span></span>
<span data-ttu-id="ae02e-130">Especifica quais usuários do SQL são excluídos do mascaramento.</span><span class="sxs-lookup"><span data-stu-id="ae02e-130">Specifies which SQL users are excluded from masking.</span></span>
<span data-ttu-id="ae02e-131">Esse parâmetro é preterido e será removido de versões futuras.</span><span class="sxs-lookup"><span data-stu-id="ae02e-131">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="ae02e-132">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="ae02e-132">-PrivilegedUsers</span></span>
<span data-ttu-id="ae02e-133">Especifica uma lista separada por ponto-e-vírgula de IDs de usuário privilegiadas.</span><span class="sxs-lookup"><span data-stu-id="ae02e-133">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="ae02e-134">Esses usuários têm permissão para exibir os dados de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="ae02e-134">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="ae02e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae02e-135">-ResourceGroupName</span></span>
<span data-ttu-id="ae02e-136">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="ae02e-136">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ae02e-137">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ae02e-137">-ServerName</span></span>
<span data-ttu-id="ae02e-138">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ae02e-138">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="ae02e-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae02e-139">-Confirm</span></span>
<span data-ttu-id="ae02e-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae02e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae02e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae02e-141">-WhatIf</span></span>
<span data-ttu-id="ae02e-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae02e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae02e-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae02e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae02e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae02e-144">CommonParameters</span></span>
<span data-ttu-id="ae02e-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae02e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae02e-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae02e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae02e-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae02e-147">INPUTS</span></span>

### <span data-ttu-id="ae02e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ae02e-148">System.String</span></span>

## <span data-ttu-id="ae02e-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae02e-149">OUTPUTS</span></span>

### <span data-ttu-id="ae02e-150">Microsoft. Azure. Commands. Sql. datamasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ae02e-150">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="ae02e-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae02e-151">NOTES</span></span>

## <span data-ttu-id="ae02e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae02e-152">RELATED LINKS</span></span>

[<span data-ttu-id="ae02e-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae02e-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="ae02e-154">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae02e-154">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae02e-155">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae02e-155">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae02e-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae02e-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae02e-157">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae02e-157">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae02e-158">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ae02e-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

