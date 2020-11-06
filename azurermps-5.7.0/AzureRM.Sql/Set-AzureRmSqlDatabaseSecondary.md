---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 2c1853de6eb11c304014ac45b5469c5699105824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428699"
---
# <span data-ttu-id="f2262-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f2262-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="f2262-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2262-102">SYNOPSIS</span></span>
<span data-ttu-id="f2262-103">Alterna um banco de dados secundário para ser primário a fim de iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="f2262-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2262-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2262-104">SYNTAX</span></span>

### <span data-ttu-id="f2262-105">Nooptionsset (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2262-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2262-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="f2262-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2262-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2262-107">DESCRIPTION</span></span>
<span data-ttu-id="f2262-108">O cmdlet **set-AzureRmSqlDatabaseSecondary** alterna um banco de dados secundário para ser primário a fim de iniciar o failover.</span><span class="sxs-lookup"><span data-stu-id="f2262-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="f2262-109">Este cmdlet foi projetado como um comando de configuração geral, mas atualmente está limitado à inicialização de failover.</span><span class="sxs-lookup"><span data-stu-id="f2262-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="f2262-110">Especifique o parâmetro *AllowDataLoss* para iniciar um failover forçado durante uma interrupção.</span><span class="sxs-lookup"><span data-stu-id="f2262-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="f2262-111">Você não precisa especificar esse parâmetro ao executar uma operação planejada, como análise de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f2262-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="f2262-112">No último caso, o banco de dados secundário é sincronizado com o primário antes de ser comutado.</span><span class="sxs-lookup"><span data-stu-id="f2262-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="f2262-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2262-113">EXAMPLES</span></span>

## <span data-ttu-id="f2262-114">OS</span><span class="sxs-lookup"><span data-stu-id="f2262-114">PARAMETERS</span></span>

### <span data-ttu-id="f2262-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="f2262-115">-AllowDataLoss</span></span>
<span data-ttu-id="f2262-116">Indica que essa operação de failover permite perda de dados.</span><span class="sxs-lookup"><span data-stu-id="f2262-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2262-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2262-117">-AsJob</span></span>
<span data-ttu-id="f2262-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f2262-118">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2262-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2262-119">-DatabaseName</span></span>
<span data-ttu-id="f2262-120">Especifica o nome do banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="f2262-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="f2262-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2262-121">-DefaultProfile</span></span>
<span data-ttu-id="f2262-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f2262-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2262-123">-Failover</span><span class="sxs-lookup"><span data-stu-id="f2262-123">-Failover</span></span>
<span data-ttu-id="f2262-124">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="f2262-124">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2262-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2262-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f2262-126">Especifica o nome do grupo de recursos ao qual o banco de dados SQL do parceiro do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f2262-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="f2262-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2262-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2262-128">Especifica o nome do grupo de recursos ao qual o secundário do banco de dados SQL do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f2262-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="f2262-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f2262-129">-ServerName</span></span>
<span data-ttu-id="f2262-130">Especifica o nome do SQL Server que hospeda o banco de dados SQL do Azure secundário.</span><span class="sxs-lookup"><span data-stu-id="f2262-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="f2262-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2262-131">-Confirm</span></span>
<span data-ttu-id="f2262-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2262-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2262-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2262-133">-WhatIf</span></span>
<span data-ttu-id="f2262-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2262-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2262-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2262-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2262-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2262-136">CommonParameters</span></span>
<span data-ttu-id="f2262-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2262-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2262-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2262-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2262-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2262-139">INPUTS</span></span>

###  
<span data-ttu-id="f2262-140">Você pode canalizar ocorrências do objeto de **banco de dados** para o banco de dados secundário para failover e fazer o banco de dados primário para esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2262-140">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="f2262-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2262-141">OUTPUTS</span></span>

###  
<span data-ttu-id="f2262-142">Esse cmdlet retorna um **ReplicationLink**.</span><span class="sxs-lookup"><span data-stu-id="f2262-142">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="f2262-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2262-143">NOTES</span></span>

## <span data-ttu-id="f2262-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2262-144">RELATED LINKS</span></span>

[<span data-ttu-id="f2262-145">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f2262-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="f2262-146">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f2262-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="f2262-147">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f2262-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
