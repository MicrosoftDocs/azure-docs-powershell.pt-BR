---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110964"
---
# <span data-ttu-id="0424c-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="0424c-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="0424c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0424c-102">SYNOPSIS</span></span>
<span data-ttu-id="0424c-103">Obtém a política de mascaramento de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0424c-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="0424c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0424c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0424c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0424c-105">DESCRIPTION</span></span>
<span data-ttu-id="0424c-106">O cmdlet **Get-AzSqlDatabaseDataMaskingPolicy** obtém a política de mascaramento de dados de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0424c-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="0424c-107">Para usar esse cmdlet, use os parâmetros *ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0424c-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="0424c-108">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="0424c-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0424c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0424c-109">EXAMPLES</span></span>

### <span data-ttu-id="0424c-110">Exemplo 1: Obter a política de mascaramento de dados para um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="0424c-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="0424c-111">Esse comando obtém a política de mascaramento de dados do banco de dados Database01 no grupo de recursos ResourceGroup01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="0424c-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="0424c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0424c-112">PARAMETERS</span></span>

### <span data-ttu-id="0424c-113">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="0424c-113">-DatabaseName</span></span>
<span data-ttu-id="0424c-114">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0424c-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="0424c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0424c-115">-DefaultProfile</span></span>
<span data-ttu-id="0424c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0424c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0424c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0424c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0424c-118">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="0424c-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0424c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0424c-119">-ServerName</span></span>
<span data-ttu-id="0424c-120">Especifica o nome do servidor onde o banco de dados está localizado.</span><span class="sxs-lookup"><span data-stu-id="0424c-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="0424c-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0424c-121">-Confirm</span></span>
<span data-ttu-id="0424c-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0424c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0424c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0424c-123">-WhatIf</span></span>
<span data-ttu-id="0424c-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0424c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0424c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0424c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0424c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0424c-126">CommonParameters</span></span>
<span data-ttu-id="0424c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0424c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0424c-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0424c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0424c-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="0424c-129">INPUTS</span></span>

### <span data-ttu-id="0424c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0424c-130">System.String</span></span>

## <span data-ttu-id="0424c-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="0424c-131">OUTPUTS</span></span>

### <span data-ttu-id="0424c-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0424c-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="0424c-133">Notas</span><span class="sxs-lookup"><span data-stu-id="0424c-133">NOTES</span></span>

## <span data-ttu-id="0424c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0424c-134">RELATED LINKS</span></span>

[<span data-ttu-id="0424c-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0424c-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0424c-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0424c-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0424c-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0424c-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0424c-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="0424c-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="0424c-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0424c-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


