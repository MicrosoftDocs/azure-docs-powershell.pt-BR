---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 1660c92ef4bef4cd832bc60506f7ef24d8927313
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441379"
---
# <span data-ttu-id="ff0b4-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff0b4-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="ff0b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff0b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0b4-103">Remove um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff0b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff0b4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff0b4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff0b4-105">DESCRIPTION</span></span>
<span data-ttu-id="ff0b4-106">O cmdlet **Remove-AzureRmSqlDatabase** remove um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="ff0b4-107">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ff0b4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff0b4-108">EXAMPLES</span></span>

### <span data-ttu-id="ff0b4-109">Exemplo 1: remover um banco de dados de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="ff0b4-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ff0b4-110">Esse comando Remove o banco de dados denominado Database01 do servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="ff0b4-111">OS</span><span class="sxs-lookup"><span data-stu-id="ff0b4-111">PARAMETERS</span></span>

### <span data-ttu-id="ff0b4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ff0b4-112">-DatabaseName</span></span>
<span data-ttu-id="ff0b4-113">Especifica o nome do banco de dados que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff0b4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ff0b4-114">-Force</span></span>
<span data-ttu-id="ff0b4-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff0b4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff0b4-116">-ResourceGroupName</span></span>
<span data-ttu-id="ff0b4-117">Especifica o nome do grupo de recursos do Azure ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-117">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ff0b4-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ff0b4-118">-ServerName</span></span>
<span data-ttu-id="ff0b4-119">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ff0b4-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff0b4-120">-Confirm</span></span>
<span data-ttu-id="ff0b4-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff0b4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff0b4-122">-WhatIf</span></span>
<span data-ttu-id="ff0b4-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff0b4-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff0b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0b4-125">-DefaultProfile</span></span>
<span data-ttu-id="ff0b4-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff0b4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0b4-127">CommonParameters</span></span>
<span data-ttu-id="ff0b4-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0b4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0b4-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff0b4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0b4-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff0b4-130">INPUTS</span></span>

### <span data-ttu-id="ff0b4-131">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ff0b4-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ff0b4-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff0b4-132">OUTPUTS</span></span>

### <span data-ttu-id="ff0b4-133">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ff0b4-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ff0b4-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff0b4-134">NOTES</span></span>

## <span data-ttu-id="ff0b4-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff0b4-135">RELATED LINKS</span></span>

[<span data-ttu-id="ff0b4-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff0b4-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff0b4-137">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff0b4-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff0b4-138">Currículo-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff0b4-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff0b4-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff0b4-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff0b4-140">Suspender-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff0b4-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff0b4-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ff0b4-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


