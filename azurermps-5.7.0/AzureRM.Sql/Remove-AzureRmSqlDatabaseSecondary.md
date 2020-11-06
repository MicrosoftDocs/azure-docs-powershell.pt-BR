---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d326abcd7cc0aee627d56250ac63d68549be610d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432871"
---
# <span data-ttu-id="add33-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="add33-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="add33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="add33-102">SYNOPSIS</span></span>
<span data-ttu-id="add33-103">Finaliza a replicação de dados entre um banco de dados SQL e o banco de dados secundário especificado.</span><span class="sxs-lookup"><span data-stu-id="add33-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="add33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="add33-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="add33-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="add33-105">DESCRIPTION</span></span>
<span data-ttu-id="add33-106">O cmdlet **Remove-AzureRmSqlDatabaseSecondary** força a rescisão de um link de replicação geográfica.</span><span class="sxs-lookup"><span data-stu-id="add33-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="add33-107">Esse cmdlet substitui o cmdlet Stop-AzureSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="add33-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="add33-108">Não há sincronização de duplicação antes do cancelamento.</span><span class="sxs-lookup"><span data-stu-id="add33-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="add33-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="add33-109">EXAMPLES</span></span>

## <span data-ttu-id="add33-110">OS</span><span class="sxs-lookup"><span data-stu-id="add33-110">PARAMETERS</span></span>

### <span data-ttu-id="add33-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="add33-111">-DatabaseName</span></span>
<span data-ttu-id="add33-112">Especifica o nome do banco de dados SQL principal do Azure que tem o link de replicação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="add33-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="add33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add33-113">-DefaultProfile</span></span>
<span data-ttu-id="add33-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="add33-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="add33-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add33-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="add33-116">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="add33-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="add33-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="add33-117">-PartnerServerName</span></span>
<span data-ttu-id="add33-118">Especifica o nome do SQL Server do parceiro.</span><span class="sxs-lookup"><span data-stu-id="add33-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="add33-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add33-119">-ResourceGroupName</span></span>
<span data-ttu-id="add33-120">Especifica o nome do grupo de recursos associado ao link de replicação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="add33-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="add33-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="add33-121">-ServerName</span></span>
<span data-ttu-id="add33-122">Especifica o nome do SQL Server que tem o link de replicação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="add33-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="add33-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="add33-123">-Confirm</span></span>
<span data-ttu-id="add33-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="add33-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="add33-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="add33-125">-WhatIf</span></span>
<span data-ttu-id="add33-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="add33-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="add33-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="add33-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="add33-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add33-128">CommonParameters</span></span>
<span data-ttu-id="add33-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add33-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add33-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add33-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add33-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="add33-131">INPUTS</span></span>

###  
<span data-ttu-id="add33-132">Você pode canalizar instâncias do objeto de **banco** de dados para o banco de dados primário ou secundário para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="add33-132">You can pipe instances of the **Database** object for the primary or secondary database to this cmdlet.</span></span>

## <span data-ttu-id="add33-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="add33-133">OUTPUTS</span></span>

###  
<span data-ttu-id="add33-134">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="add33-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="add33-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="add33-135">NOTES</span></span>

## <span data-ttu-id="add33-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="add33-136">RELATED LINKS</span></span>

[<span data-ttu-id="add33-137">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="add33-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="add33-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="add33-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="add33-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="add33-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
