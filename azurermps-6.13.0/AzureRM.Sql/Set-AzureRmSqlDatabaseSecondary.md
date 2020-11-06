---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 56749c265980fc40ee19b60261641f0c98c25da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430821"
---
# <span data-ttu-id="54e01-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="54e01-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="54e01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54e01-102">SYNOPSIS</span></span>
<span data-ttu-id="54e01-103">Alterna um banco de dados secundário para ser primário a fim de iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="54e01-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54e01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54e01-104">SYNTAX</span></span>

### <span data-ttu-id="54e01-105">Nooptionsset (padrão)</span><span class="sxs-lookup"><span data-stu-id="54e01-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54e01-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="54e01-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e01-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54e01-107">DESCRIPTION</span></span>
<span data-ttu-id="54e01-108">O cmdlet **set-AzureRmSqlDatabaseSecondary** alterna um banco de dados secundário para ser primário a fim de iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="54e01-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="54e01-109">Este cmdlet foi projetado como um comando de configuração geral, mas atualmente está limitado à inicialização de failover.</span><span class="sxs-lookup"><span data-stu-id="54e01-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="54e01-110">Especifique o parâmetro *AllowDataLoss* para iniciar um failover forçado durante uma interrupção.</span><span class="sxs-lookup"><span data-stu-id="54e01-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="54e01-111">Você não precisa especificar esse parâmetro ao executar uma operação planejada, como análise de recuperação.</span><span class="sxs-lookup"><span data-stu-id="54e01-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="54e01-112">No último caso, o banco de dados secundário é sincronizado com o primário antes de ser comutado.</span><span class="sxs-lookup"><span data-stu-id="54e01-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="54e01-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54e01-113">EXAMPLES</span></span>

## <span data-ttu-id="54e01-114">OS</span><span class="sxs-lookup"><span data-stu-id="54e01-114">PARAMETERS</span></span>

### <span data-ttu-id="54e01-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="54e01-115">-AllowDataLoss</span></span>
<span data-ttu-id="54e01-116">Indica que essa operação de failover permite perda de dados.</span><span class="sxs-lookup"><span data-stu-id="54e01-116">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="54e01-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54e01-117">-AsJob</span></span>
<span data-ttu-id="54e01-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="54e01-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54e01-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="54e01-119">-DatabaseName</span></span>
<span data-ttu-id="54e01-120">Especifica o nome do banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="54e01-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="54e01-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e01-121">-DefaultProfile</span></span>
<span data-ttu-id="54e01-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="54e01-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54e01-123">-Failover</span><span class="sxs-lookup"><span data-stu-id="54e01-123">-Failover</span></span>
<span data-ttu-id="54e01-124">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="54e01-124">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="54e01-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e01-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="54e01-126">Especifica o nome do grupo de recursos ao qual o banco de dados SQL do parceiro do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="54e01-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="54e01-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e01-127">-ResourceGroupName</span></span>
<span data-ttu-id="54e01-128">Especifica o nome do grupo de recursos ao qual o secundário do banco de dados SQL do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="54e01-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="54e01-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="54e01-129">-ServerName</span></span>
<span data-ttu-id="54e01-130">Especifica o nome do SQL Server que hospeda o banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="54e01-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="54e01-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54e01-131">-Confirm</span></span>
<span data-ttu-id="54e01-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54e01-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e01-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e01-133">-WhatIf</span></span>
<span data-ttu-id="54e01-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54e01-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e01-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54e01-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e01-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e01-136">CommonParameters</span></span>
<span data-ttu-id="54e01-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e01-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e01-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e01-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e01-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54e01-139">INPUTS</span></span>

### <span data-ttu-id="54e01-140">System. String</span><span class="sxs-lookup"><span data-stu-id="54e01-140">System.String</span></span>

## <span data-ttu-id="54e01-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54e01-141">OUTPUTS</span></span>

### <span data-ttu-id="54e01-142">Microsoft. Azure. Commands. Sql. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="54e01-142">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="54e01-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54e01-143">NOTES</span></span>

## <span data-ttu-id="54e01-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54e01-144">RELATED LINKS</span></span>

[<span data-ttu-id="54e01-145">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="54e01-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="54e01-146">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="54e01-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="54e01-147">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="54e01-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
