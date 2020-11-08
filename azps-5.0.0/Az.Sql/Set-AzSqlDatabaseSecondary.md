---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115649"
---
# <span data-ttu-id="b34a4-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b34a4-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b34a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b34a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b34a4-103">Alterna um banco de dados secundário para ser primário a fim de iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="b34a4-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="b34a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b34a4-104">SYNTAX</span></span>

### <span data-ttu-id="b34a4-105">Nooptionsset (padrão)</span><span class="sxs-lookup"><span data-stu-id="b34a4-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b34a4-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="b34a4-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b34a4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b34a4-107">DESCRIPTION</span></span>
<span data-ttu-id="b34a4-108">O cmdlet **set-AzSqlDatabaseSecondary** alterna um banco de dados secundário para ser primário a fim de iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="b34a4-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="b34a4-109">Este cmdlet foi projetado como um comando de configuração geral, mas atualmente está limitado à inicialização de failover.</span><span class="sxs-lookup"><span data-stu-id="b34a4-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="b34a4-110">Especifique o parâmetro *AllowDataLoss* para iniciar um failover forçado durante uma interrupção.</span><span class="sxs-lookup"><span data-stu-id="b34a4-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="b34a4-111">Você não precisa especificar esse parâmetro ao executar uma operação planejada, como análise de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b34a4-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="b34a4-112">No último caso, o banco de dados secundário é sincronizado com o primário antes de ser comutado.</span><span class="sxs-lookup"><span data-stu-id="b34a4-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="b34a4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b34a4-113">EXAMPLES</span></span>

### <span data-ttu-id="b34a4-114">Exemplo 1: iniciar um failover planejado</span><span class="sxs-lookup"><span data-stu-id="b34a4-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="b34a4-115">Exemplo 2: iniciar um failover forçado (com potencial perda de dados)</span><span class="sxs-lookup"><span data-stu-id="b34a4-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="b34a4-116">OS</span><span class="sxs-lookup"><span data-stu-id="b34a4-116">PARAMETERS</span></span>

### <span data-ttu-id="b34a4-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="b34a4-117">-AllowDataLoss</span></span>
<span data-ttu-id="b34a4-118">Indica que essa operação de failover permite perda de dados.</span><span class="sxs-lookup"><span data-stu-id="b34a4-118">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="b34a4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b34a4-119">-AsJob</span></span>
<span data-ttu-id="b34a4-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b34a4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b34a4-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b34a4-121">-DatabaseName</span></span>
<span data-ttu-id="b34a4-122">Especifica o nome do banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="b34a4-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="b34a4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34a4-123">-DefaultProfile</span></span>
<span data-ttu-id="b34a4-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b34a4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b34a4-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="b34a4-125">-Failover</span></span>
<span data-ttu-id="b34a4-126">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="b34a4-126">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="b34a4-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34a4-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b34a4-128">Especifica o nome do grupo de recursos ao qual o banco de dados SQL do parceiro do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b34a4-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="b34a4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34a4-129">-ResourceGroupName</span></span>
<span data-ttu-id="b34a4-130">Especifica o nome do grupo de recursos ao qual o secundário do banco de dados SQL do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b34a4-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="b34a4-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b34a4-131">-ServerName</span></span>
<span data-ttu-id="b34a4-132">Especifica o nome do SQL Server que hospeda o banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="b34a4-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="b34a4-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b34a4-133">-Confirm</span></span>
<span data-ttu-id="b34a4-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b34a4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b34a4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b34a4-135">-WhatIf</span></span>
<span data-ttu-id="b34a4-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b34a4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34a4-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b34a4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b34a4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34a4-138">CommonParameters</span></span>
<span data-ttu-id="b34a4-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34a4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34a4-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b34a4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34a4-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b34a4-141">INPUTS</span></span>

### <span data-ttu-id="b34a4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b34a4-142">System.String</span></span>

## <span data-ttu-id="b34a4-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b34a4-143">OUTPUTS</span></span>

### <span data-ttu-id="b34a4-144">Microsoft. Azure. Commands. Sql. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="b34a4-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="b34a4-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b34a4-145">NOTES</span></span>

## <span data-ttu-id="b34a4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b34a4-146">RELATED LINKS</span></span>

[<span data-ttu-id="b34a4-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b34a4-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="b34a4-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b34a4-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="b34a4-149">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b34a4-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
