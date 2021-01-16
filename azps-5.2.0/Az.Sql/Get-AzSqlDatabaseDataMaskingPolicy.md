---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263844"
---
# <span data-ttu-id="32230-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="32230-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="32230-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32230-102">SYNOPSIS</span></span>
<span data-ttu-id="32230-103">Obtém a política de máscara de dados de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="32230-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="32230-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32230-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32230-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32230-105">DESCRIPTION</span></span>
<span data-ttu-id="32230-106">O cmdlet **Get-AzSqlDatabaseDataMaskingPolicy** Obtém a política de máscara de dados de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="32230-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="32230-107">Para usar esse cmdlet, use os parâmetros *ResourceGroupName*, *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="32230-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="32230-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="32230-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="32230-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32230-109">EXAMPLES</span></span>

### <span data-ttu-id="32230-110">Exemplo 1: obter a política de máscara de dados de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="32230-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="32230-111">Esse comando obtém a política de máscara de dados do banco de dados Database01 no grupo ResourceGroup01 de recursos no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="32230-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="32230-112">OS</span><span class="sxs-lookup"><span data-stu-id="32230-112">PARAMETERS</span></span>

### <span data-ttu-id="32230-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32230-113">-DatabaseName</span></span>
<span data-ttu-id="32230-114">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="32230-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="32230-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32230-115">-DefaultProfile</span></span>
<span data-ttu-id="32230-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="32230-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32230-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32230-117">-ResourceGroupName</span></span>
<span data-ttu-id="32230-118">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="32230-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="32230-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="32230-119">-ServerName</span></span>
<span data-ttu-id="32230-120">Especifica o nome do servidor no qual o banco de dados está localizado.</span><span class="sxs-lookup"><span data-stu-id="32230-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="32230-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32230-121">-Confirm</span></span>
<span data-ttu-id="32230-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32230-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32230-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32230-123">-WhatIf</span></span>
<span data-ttu-id="32230-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32230-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32230-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32230-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32230-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32230-126">CommonParameters</span></span>
<span data-ttu-id="32230-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32230-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32230-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32230-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32230-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32230-129">INPUTS</span></span>

### <span data-ttu-id="32230-130">System. String</span><span class="sxs-lookup"><span data-stu-id="32230-130">System.String</span></span>

## <span data-ttu-id="32230-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32230-131">OUTPUTS</span></span>

### <span data-ttu-id="32230-132">Microsoft. Azure. Commands. Sql. datamasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="32230-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="32230-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32230-133">NOTES</span></span>

## <span data-ttu-id="32230-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32230-134">RELATED LINKS</span></span>

[<span data-ttu-id="32230-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="32230-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="32230-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="32230-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="32230-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="32230-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="32230-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="32230-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="32230-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="32230-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


