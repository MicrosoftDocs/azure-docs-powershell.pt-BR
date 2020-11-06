---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609479"
---
# <span data-ttu-id="81076-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="81076-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="81076-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81076-102">SYNOPSIS</span></span>
<span data-ttu-id="81076-103">Cria um novo ponto de restauração a partir do qual um banco de dados SQL pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="81076-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81076-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81076-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81076-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81076-105">DESCRIPTION</span></span>
<span data-ttu-id="81076-106">O cmdlet **New-AzureRmSqlDatabaseRestorePoint** cria um novo ponto de restauração do qual um banco de dados SQL do Azure pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="81076-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="81076-107">No momento, esse cmdlet é compatível com o serviço SQL Server DataWarehouse no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="81076-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="81076-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81076-108">EXAMPLES</span></span>

### <span data-ttu-id="81076-109">Exemplo 1: criar um ponto de restauração</span><span class="sxs-lookup"><span data-stu-id="81076-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="81076-110">Esse comando cria um ponto de restauração para o banco de dados SQL do Azure e retorna os detalhes do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="81076-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="81076-111">OS</span><span class="sxs-lookup"><span data-stu-id="81076-111">PARAMETERS</span></span>

### <span data-ttu-id="81076-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81076-112">-DatabaseName</span></span>
<span data-ttu-id="81076-113">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="81076-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="81076-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81076-114">-DefaultProfile</span></span>
<span data-ttu-id="81076-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="81076-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81076-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81076-116">-ResourceGroupName</span></span>
<span data-ttu-id="81076-117">Especifica o nome do grupo de recursos ao qual o banco de dados do SQL está atribuído.</span><span class="sxs-lookup"><span data-stu-id="81076-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="81076-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="81076-118">-RestorePointLabel</span></span>
<span data-ttu-id="81076-119">Especifica o rótulo do ponto de restauração para facilitar a identificação.</span><span class="sxs-lookup"><span data-stu-id="81076-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81076-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="81076-120">-ServerName</span></span>
<span data-ttu-id="81076-121">Especifica o nome do servidor AzureSQL que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81076-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="81076-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81076-122">-Confirm</span></span>
<span data-ttu-id="81076-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81076-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81076-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81076-124">-WhatIf</span></span>
<span data-ttu-id="81076-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81076-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81076-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81076-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81076-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81076-127">CommonParameters</span></span>
<span data-ttu-id="81076-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81076-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81076-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81076-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81076-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81076-130">INPUTS</span></span>

## <span data-ttu-id="81076-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81076-131">OUTPUTS</span></span>

## <span data-ttu-id="81076-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81076-132">NOTES</span></span>

## <span data-ttu-id="81076-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81076-133">RELATED LINKS</span></span>
