---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
ms.openlocfilehash: b3b09e9027a578809fe68a90630331ad6ee35943
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440931"
---
# <span data-ttu-id="5f32f-101">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="5f32f-101">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>

## <span data-ttu-id="5f32f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f32f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f32f-103">Obtém as operações de índice recomendadas para um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5f32f-103">Gets the recommended index operations for a server or database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f32f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f32f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseIndexRecommendations -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f32f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f32f-105">DESCRIPTION</span></span>
<span data-ttu-id="5f32f-106">O cmdlet **Get-AzureRmSqlDatabaseIndexRecommendations** Obtém as operações de índice recomendadas para um banco de dados ou um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f32f-106">The **Get-AzureRmSqlDatabaseIndexRecommendations** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="5f32f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f32f-107">EXAMPLES</span></span>

### <span data-ttu-id="5f32f-108">Exemplo 1: obter recomendações de índice para todos os bancos de dados no servidor</span><span class="sxs-lookup"><span data-stu-id="5f32f-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="5f32f-109">Esse comando retorna recomendações de índice para todos os bancos de dados no Server Server01.</span><span class="sxs-lookup"><span data-stu-id="5f32f-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="5f32f-110">Exemplo 2: obter recomendações de índice para um banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="5f32f-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5f32f-111">Esse comando retorna recomendações de índice para um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="5f32f-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="5f32f-112">Exemplo 3: obter uma única recomendação de índice por nome</span><span class="sxs-lookup"><span data-stu-id="5f32f-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="5f32f-113">Esse comando retorna a recomendação de índice único por nome.</span><span class="sxs-lookup"><span data-stu-id="5f32f-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="5f32f-114">OS</span><span class="sxs-lookup"><span data-stu-id="5f32f-114">PARAMETERS</span></span>

### <span data-ttu-id="5f32f-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f32f-115">-DatabaseName</span></span>
<span data-ttu-id="5f32f-116">Especifica o nome do banco de dados para o qual este cmdlet obtém recomendações de índice.</span><span class="sxs-lookup"><span data-stu-id="5f32f-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="5f32f-117">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="5f32f-117">-IndexRecommendationName</span></span>
<span data-ttu-id="5f32f-118">Especifica o nome da recomendação de índice que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5f32f-118">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f32f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f32f-119">-ResourceGroupName</span></span>
<span data-ttu-id="5f32f-120">Especifica o nome do grupo de recursos para o qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="5f32f-120">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="5f32f-121">Este cmdlet obtém recomendações de índice para um banco de dados hospedado por esse servidor.</span><span class="sxs-lookup"><span data-stu-id="5f32f-121">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="5f32f-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5f32f-122">-ServerName</span></span>
<span data-ttu-id="5f32f-123">Especifica o servidor que hospeda o banco de dados para o qual esse cmdlet obtém recomendações de índice.</span><span class="sxs-lookup"><span data-stu-id="5f32f-123">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="5f32f-124">-TableName</span><span class="sxs-lookup"><span data-stu-id="5f32f-124">-TableName</span></span>
<span data-ttu-id="5f32f-125">Especifica o nome de uma tabela SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f32f-125">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="5f32f-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5f32f-126">-Confirm</span></span>
<span data-ttu-id="5f32f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f32f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f32f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f32f-128">-WhatIf</span></span>
<span data-ttu-id="5f32f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5f32f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f32f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5f32f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f32f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f32f-131">-DefaultProfile</span></span>
<span data-ttu-id="5f32f-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f32f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f32f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f32f-133">CommonParameters</span></span>
<span data-ttu-id="5f32f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f32f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f32f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f32f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f32f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f32f-136">INPUTS</span></span>

## <span data-ttu-id="5f32f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f32f-137">OUTPUTS</span></span>

## <span data-ttu-id="5f32f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f32f-138">NOTES</span></span>

## <span data-ttu-id="5f32f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f32f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5f32f-140">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="5f32f-140">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="5f32f-141">Parar-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="5f32f-141">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)
