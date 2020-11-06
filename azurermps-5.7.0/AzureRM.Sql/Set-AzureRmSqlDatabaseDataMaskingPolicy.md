---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 26d056b5ad9cdff22f0419f90fad17c3147e0e14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428704"
---
# <span data-ttu-id="3a00e-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="3a00e-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="3a00e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a00e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a00e-103">Define o mascaramento de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a00e-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a00e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a00e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a00e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a00e-105">DESCRIPTION</span></span>
<span data-ttu-id="3a00e-106">O cmdlet **set-AzureRmSqlDatabaseDataMaskingPolicy** define a política de máscara de dados de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a00e-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="3a00e-107">Para usar esse cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a00e-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="3a00e-108">Você pode definir o parâmetro *DataMaskingState* para especificar se as operações de máscara de dados estão habilitadas ou desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="3a00e-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="3a00e-109">Você também pode definir o parâmetro *PrivilegedLogins* para especificar quais usuários têm permissão para ver os dados não mascarados.</span><span class="sxs-lookup"><span data-stu-id="3a00e-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="3a00e-110">Se o cmdlet for bem-sucedido e o parâmetro *PassThru* for usado, ele retornará um objeto que descreve a política de mascaramento de dados atual, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a00e-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="3a00e-111">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="3a00e-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="3a00e-112">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="3a00e-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3a00e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a00e-113">EXAMPLES</span></span>

### <span data-ttu-id="3a00e-114">Exemplo 1: definir a política de máscara de dados para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="3a00e-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="3a00e-115">Esse comando define a política de máscara de dados para um banco de dados denominado database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="3a00e-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="3a00e-116">OS</span><span class="sxs-lookup"><span data-stu-id="3a00e-116">PARAMETERS</span></span>

### <span data-ttu-id="3a00e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a00e-117">-DatabaseName</span></span>
<span data-ttu-id="3a00e-118">Especifica o nome do banco de dados onde a política está definida.</span><span class="sxs-lookup"><span data-stu-id="3a00e-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="3a00e-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="3a00e-119">-DataMaskingState</span></span>
<span data-ttu-id="3a00e-120">Especifica se a operação de máscara de dados está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="3a00e-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="3a00e-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3a00e-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a00e-122">Possibilita</span><span class="sxs-lookup"><span data-stu-id="3a00e-122">Enabled</span></span>
- <span data-ttu-id="3a00e-123">Ativo</span><span class="sxs-lookup"><span data-stu-id="3a00e-123">Disabled</span></span>

<span data-ttu-id="3a00e-124">O valor padrão é habilitado.</span><span class="sxs-lookup"><span data-stu-id="3a00e-124">The default value is Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a00e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a00e-125">-DefaultProfile</span></span>
<span data-ttu-id="3a00e-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3a00e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a00e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a00e-127">-PassThru</span></span>
<span data-ttu-id="3a00e-128">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3a00e-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a00e-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3a00e-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a00e-130">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="3a00e-130">-PrivilegedLogins</span></span>
<span data-ttu-id="3a00e-131">Especifica quais usuários do SQL são excluídos do mascaramento.</span><span class="sxs-lookup"><span data-stu-id="3a00e-131">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="3a00e-132">Esse parâmetro é preterido e será removido de versões futuras.</span><span class="sxs-lookup"><span data-stu-id="3a00e-132">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a00e-133">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="3a00e-133">-PrivilegedUsers</span></span>
<span data-ttu-id="3a00e-134">Especifica uma lista separada por ponto-e-vírgula de IDs de usuário privilegiadas.</span><span class="sxs-lookup"><span data-stu-id="3a00e-134">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="3a00e-135">Esses usuários têm permissão para exibir os dados de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="3a00e-135">These users are allowed to view the masking data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a00e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a00e-136">-ResourceGroupName</span></span>
<span data-ttu-id="3a00e-137">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="3a00e-137">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3a00e-138">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3a00e-138">-ServerName</span></span>
<span data-ttu-id="3a00e-139">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a00e-139">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="3a00e-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a00e-140">-Confirm</span></span>
<span data-ttu-id="3a00e-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a00e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a00e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a00e-142">-WhatIf</span></span>
<span data-ttu-id="3a00e-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a00e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a00e-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a00e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a00e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a00e-145">CommonParameters</span></span>
<span data-ttu-id="3a00e-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a00e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a00e-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a00e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a00e-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a00e-148">INPUTS</span></span>

### <span data-ttu-id="3a00e-149">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3a00e-149">None</span></span>
<span data-ttu-id="3a00e-150">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3a00e-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a00e-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a00e-151">OUTPUTS</span></span>

### <span data-ttu-id="3a00e-152">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3a00e-152">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="3a00e-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a00e-153">NOTES</span></span>

## <span data-ttu-id="3a00e-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a00e-154">RELATED LINKS</span></span>

[<span data-ttu-id="3a00e-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="3a00e-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="3a00e-156">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3a00e-156">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3a00e-157">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3a00e-157">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3a00e-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3a00e-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3a00e-159">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="3a00e-159">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="3a00e-160">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3a00e-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


