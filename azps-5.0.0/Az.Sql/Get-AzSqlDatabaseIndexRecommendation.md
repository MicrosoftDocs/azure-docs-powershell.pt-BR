---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115669"
---
# <span data-ttu-id="984ef-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="984ef-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="984ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="984ef-102">SYNOPSIS</span></span>
<span data-ttu-id="984ef-103">Obtém as operações de índice recomendadas para um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="984ef-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="984ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="984ef-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="984ef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="984ef-105">DESCRIPTION</span></span>
<span data-ttu-id="984ef-106">O cmdlet **Get-AzSqlDatabaseIndexRecommendation** Obtém as operações de índice recomendadas para um banco de dados ou um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="984ef-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="984ef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="984ef-107">EXAMPLES</span></span>

### <span data-ttu-id="984ef-108">Exemplo 1: obter recomendações de índice para todos os bancos de dados no servidor</span><span class="sxs-lookup"><span data-stu-id="984ef-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="984ef-109">Esse comando retorna recomendações de índice para todos os bancos de dados no Server Server01.</span><span class="sxs-lookup"><span data-stu-id="984ef-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="984ef-110">Exemplo 2: obter recomendações de índice para um banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="984ef-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="984ef-111">Esse comando retorna recomendações de índice para um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="984ef-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="984ef-112">Exemplo 3: obter uma única recomendação de índice por nome</span><span class="sxs-lookup"><span data-stu-id="984ef-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="984ef-113">Esse comando retorna a recomendação de índice único por nome.</span><span class="sxs-lookup"><span data-stu-id="984ef-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="984ef-114">OS</span><span class="sxs-lookup"><span data-stu-id="984ef-114">PARAMETERS</span></span>

### <span data-ttu-id="984ef-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="984ef-115">-DatabaseName</span></span>
<span data-ttu-id="984ef-116">Especifica o nome do banco de dados para o qual este cmdlet obtém recomendações de índice.</span><span class="sxs-lookup"><span data-stu-id="984ef-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="984ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984ef-117">-DefaultProfile</span></span>
<span data-ttu-id="984ef-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="984ef-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="984ef-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="984ef-119">-IndexRecommendationName</span></span>
<span data-ttu-id="984ef-120">Especifica o nome da recomendação de índice que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="984ef-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="984ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="984ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="984ef-122">Especifica o nome do grupo de recursos para o qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="984ef-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="984ef-123">Este cmdlet obtém recomendações de índice para um banco de dados hospedado por esse servidor.</span><span class="sxs-lookup"><span data-stu-id="984ef-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="984ef-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="984ef-124">-ServerName</span></span>
<span data-ttu-id="984ef-125">Especifica o servidor que hospeda o banco de dados para o qual esse cmdlet obtém recomendações de índice.</span><span class="sxs-lookup"><span data-stu-id="984ef-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="984ef-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="984ef-126">-TableName</span></span>
<span data-ttu-id="984ef-127">Especifica o nome de uma tabela SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="984ef-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="984ef-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="984ef-128">-Confirm</span></span>
<span data-ttu-id="984ef-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="984ef-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="984ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="984ef-130">-WhatIf</span></span>
<span data-ttu-id="984ef-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="984ef-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="984ef-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="984ef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="984ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984ef-133">CommonParameters</span></span>
<span data-ttu-id="984ef-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="984ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984ef-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="984ef-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984ef-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="984ef-136">INPUTS</span></span>

### <span data-ttu-id="984ef-137">System. String</span><span class="sxs-lookup"><span data-stu-id="984ef-137">System.String</span></span>

## <span data-ttu-id="984ef-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="984ef-138">OUTPUTS</span></span>

### <span data-ttu-id="984ef-139">Microsoft. Azure. Commands. Sql. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="984ef-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="984ef-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="984ef-140">NOTES</span></span>

## <span data-ttu-id="984ef-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="984ef-141">RELATED LINKS</span></span>

[<span data-ttu-id="984ef-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="984ef-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="984ef-143">Parar-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="984ef-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
