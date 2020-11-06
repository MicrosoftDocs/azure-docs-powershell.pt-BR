---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a6fd65ed16797d3d497160f7f7d9d52f17bd2f1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432879"
---
# <span data-ttu-id="bdc05-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bdc05-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="bdc05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdc05-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc05-103">Remove um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc05-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdc05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdc05-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdc05-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdc05-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc05-106">Esse comando Remove o grupo de failover com o nome especificado, deixando todos os bancos de dados e relações de replicação intactos.</span><span class="sxs-lookup"><span data-stu-id="bdc05-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="bdc05-107">O ponto de extremidade de escuta será cancelado do DNS.</span><span class="sxs-lookup"><span data-stu-id="bdc05-107">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="bdc05-108">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="bdc05-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="bdc05-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdc05-109">EXAMPLES</span></span>

### <span data-ttu-id="bdc05-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bdc05-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="bdc05-111">Remover um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="bdc05-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="bdc05-112">OS</span><span class="sxs-lookup"><span data-stu-id="bdc05-112">PARAMETERS</span></span>

### <span data-ttu-id="bdc05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc05-113">-DefaultProfile</span></span>
<span data-ttu-id="bdc05-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bdc05-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdc05-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc05-115">-FailoverGroupName</span></span>
<span data-ttu-id="bdc05-116">O nome do grupo de failover de banco de dados SQL do Azure a ser removido.</span><span class="sxs-lookup"><span data-stu-id="bdc05-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="bdc05-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bdc05-117">-Force</span></span>
<span data-ttu-id="bdc05-118">Ignore a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="bdc05-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdc05-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc05-119">-ResourceGroupName</span></span>
<span data-ttu-id="bdc05-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdc05-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="bdc05-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="bdc05-121">-ServerName</span></span>
<span data-ttu-id="bdc05-122">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="bdc05-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="bdc05-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bdc05-123">-Confirm</span></span>
<span data-ttu-id="bdc05-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc05-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc05-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc05-125">-WhatIf</span></span>
<span data-ttu-id="bdc05-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdc05-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc05-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdc05-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc05-128">CommonParameters</span></span>
<span data-ttu-id="bdc05-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc05-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc05-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc05-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdc05-131">INPUTS</span></span>

### <span data-ttu-id="bdc05-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bdc05-132">System.String</span></span>

## <span data-ttu-id="bdc05-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdc05-133">OUTPUTS</span></span>

### <span data-ttu-id="bdc05-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="bdc05-134">System.Object</span></span>

## <span data-ttu-id="bdc05-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdc05-135">NOTES</span></span>

## <span data-ttu-id="bdc05-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdc05-136">RELATED LINKS</span></span>

[<span data-ttu-id="bdc05-137">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bdc05-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bdc05-138">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bdc05-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bdc05-139">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bdc05-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bdc05-140">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bdc05-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="bdc05-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bdc05-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="bdc05-142">Botão de AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bdc05-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="bdc05-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="bdc05-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
