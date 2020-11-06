---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 598266c17bde6cb9e05efa6b917341975f0a3153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598785"
---
# <span data-ttu-id="50be9-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="50be9-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="50be9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50be9-102">SYNOPSIS</span></span>
<span data-ttu-id="50be9-103">Alterna um banco de dados secundário para ser primário a fim de iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="50be9-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="50be9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50be9-104">SYNTAX</span></span>

### <span data-ttu-id="50be9-105">Nooptionsset (padrão)</span><span class="sxs-lookup"><span data-stu-id="50be9-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50be9-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="50be9-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50be9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50be9-107">DESCRIPTION</span></span>
<span data-ttu-id="50be9-108">O cmdlet **set-AzSqlDatabaseSecondary** alterna um banco de dados secundário para ser primário a fim de iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="50be9-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="50be9-109">Este cmdlet foi projetado como um comando de configuração geral, mas atualmente está limitado à inicialização de failover.</span><span class="sxs-lookup"><span data-stu-id="50be9-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="50be9-110">Especifique o parâmetro *AllowDataLoss* para iniciar um failover forçado durante uma interrupção.</span><span class="sxs-lookup"><span data-stu-id="50be9-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="50be9-111">Você não precisa especificar esse parâmetro ao executar uma operação planejada, como análise de recuperação.</span><span class="sxs-lookup"><span data-stu-id="50be9-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="50be9-112">No último caso, o banco de dados secundário é sincronizado com o primário antes de ser comutado.</span><span class="sxs-lookup"><span data-stu-id="50be9-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="50be9-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50be9-113">EXAMPLES</span></span>

## <span data-ttu-id="50be9-114">OS</span><span class="sxs-lookup"><span data-stu-id="50be9-114">PARAMETERS</span></span>

### <span data-ttu-id="50be9-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="50be9-115">-AllowDataLoss</span></span>
<span data-ttu-id="50be9-116">Indica que essa operação de failover permite perda de dados.</span><span class="sxs-lookup"><span data-stu-id="50be9-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50be9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50be9-117">-AsJob</span></span>
<span data-ttu-id="50be9-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="50be9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50be9-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="50be9-119">-DatabaseName</span></span>
<span data-ttu-id="50be9-120">Especifica o nome do banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="50be9-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="50be9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50be9-121">-DefaultProfile</span></span>
<span data-ttu-id="50be9-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="50be9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50be9-123">-Failover</span><span class="sxs-lookup"><span data-stu-id="50be9-123">-Failover</span></span>
<span data-ttu-id="50be9-124">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="50be9-124">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50be9-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50be9-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="50be9-126">Especifica o nome do grupo de recursos ao qual o banco de dados SQL do parceiro do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="50be9-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="50be9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50be9-127">-ResourceGroupName</span></span>
<span data-ttu-id="50be9-128">Especifica o nome do grupo de recursos ao qual o secundário do banco de dados SQL do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="50be9-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="50be9-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="50be9-129">-ServerName</span></span>
<span data-ttu-id="50be9-130">Especifica o nome do SQL Server que hospeda o banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="50be9-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="50be9-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="50be9-131">-Confirm</span></span>
<span data-ttu-id="50be9-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50be9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50be9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50be9-133">-WhatIf</span></span>
<span data-ttu-id="50be9-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="50be9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50be9-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="50be9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50be9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50be9-136">CommonParameters</span></span>
<span data-ttu-id="50be9-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50be9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50be9-138">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50be9-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50be9-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50be9-139">INPUTS</span></span>

### <span data-ttu-id="50be9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="50be9-140">System.String</span></span>

## <span data-ttu-id="50be9-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50be9-141">OUTPUTS</span></span>

### <span data-ttu-id="50be9-142">Microsoft. Azure. Commands. Sql. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="50be9-142">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="50be9-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50be9-143">NOTES</span></span>

## <span data-ttu-id="50be9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50be9-144">RELATED LINKS</span></span>

[<span data-ttu-id="50be9-145">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="50be9-145">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="50be9-146">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="50be9-146">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="50be9-147">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="50be9-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
