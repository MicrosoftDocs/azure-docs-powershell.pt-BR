---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: f2ee19834cdb4144c8f207ae8ff10a90a733bece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430019"
---
# <span data-ttu-id="d74e4-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="d74e4-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="d74e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d74e4-102">SYNOPSIS</span></span>
<span data-ttu-id="d74e4-103">Obtém um banco de dados e seus valores de propriedade expandida.</span><span class="sxs-lookup"><span data-stu-id="d74e4-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d74e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d74e4-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d74e4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d74e4-105">DESCRIPTION</span></span>
<span data-ttu-id="d74e4-106">O cmdlet **Get-AzureRmSqlDatabaseExpanded** Obtém um banco de dados e seus valores de propriedade expandida.</span><span class="sxs-lookup"><span data-stu-id="d74e4-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="d74e4-107">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="d74e4-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d74e4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d74e4-108">EXAMPLES</span></span>

### <span data-ttu-id="d74e4-109">Exemplo 1: obter objeto de banco de dados com informações do supervisor da camada de serviço</span><span class="sxs-lookup"><span data-stu-id="d74e4-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d74e4-110">Esse comando retorna o banco de dados que tem propriedades expandidas que contêm as informações do supervisor da camada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d74e4-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="d74e4-111">OS</span><span class="sxs-lookup"><span data-stu-id="d74e4-111">PARAMETERS</span></span>

### <span data-ttu-id="d74e4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d74e4-112">-DatabaseName</span></span>
<span data-ttu-id="d74e4-113">Especifica o nome do banco de dados a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="d74e4-113">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d74e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74e4-114">-DefaultProfile</span></span>
<span data-ttu-id="d74e4-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d74e4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d74e4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d74e4-116">-ResourceGroupName</span></span>
<span data-ttu-id="d74e4-117">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="d74e4-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d74e4-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d74e4-118">-ServerName</span></span>
<span data-ttu-id="d74e4-119">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d74e4-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d74e4-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d74e4-120">-Confirm</span></span>
<span data-ttu-id="d74e4-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d74e4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74e4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74e4-122">-WhatIf</span></span>
<span data-ttu-id="d74e4-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d74e4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d74e4-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d74e4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74e4-125">CommonParameters</span></span>
<span data-ttu-id="d74e4-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d74e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74e4-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d74e4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74e4-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d74e4-128">INPUTS</span></span>

### <span data-ttu-id="d74e4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d74e4-129">System.String</span></span>

## <span data-ttu-id="d74e4-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d74e4-130">OUTPUTS</span></span>

### <span data-ttu-id="d74e4-131">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="d74e4-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="d74e4-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d74e4-132">NOTES</span></span>

## <span data-ttu-id="d74e4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d74e4-133">RELATED LINKS</span></span>

[<span data-ttu-id="d74e4-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d74e4-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
