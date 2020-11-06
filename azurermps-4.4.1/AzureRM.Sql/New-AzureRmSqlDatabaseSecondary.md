---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 226910b81da287c04adb05574b77713e97c6a045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602190"
---
# <span data-ttu-id="8ce8a-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8ce8a-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="8ce8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ce8a-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce8a-103">Cria um banco de dados secundário para um banco de dados existente e inicia a replicação de dados.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ce8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ce8a-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ce8a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ce8a-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce8a-106">O cmdlet **New-AzureRMSqlDatabaseSecondary** substitui o cmdlet Start-AzureSqlDatabaseCopy quando usado para configurar a replicação geográfica para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="8ce8a-107">Ele retorna o objeto de link de replicação geográfica do banco de dados primário para o secundário.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="8ce8a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ce8a-108">EXAMPLES</span></span>

### <span data-ttu-id="8ce8a-109">1: estabelecer Geo-Replication ativas</span><span class="sxs-lookup"><span data-stu-id="8ce8a-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="8ce8a-110">OS</span><span class="sxs-lookup"><span data-stu-id="8ce8a-110">PARAMETERS</span></span>

### <span data-ttu-id="8ce8a-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="8ce8a-111">-AllowConnections</span></span>
<span data-ttu-id="8ce8a-112">Especifica a intenção de leitura do banco de dados SQL secundário do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="8ce8a-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8ce8a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8ce8a-114">Não</span><span class="sxs-lookup"><span data-stu-id="8ce8a-114">No</span></span>
- <span data-ttu-id="8ce8a-115">Todo</span><span class="sxs-lookup"><span data-stu-id="8ce8a-115">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases: 
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce8a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8ce8a-116">-DatabaseName</span></span>
<span data-ttu-id="8ce8a-117">Especifica o nome do banco de dados para atuar como primário.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-117">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="8ce8a-118">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce8a-118">-PartnerResourceGroupName</span></span>
<span data-ttu-id="8ce8a-119">Especifica o nome do grupo de recursos do Azure ao qual esse cmdlet atribui o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-119">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce8a-120">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="8ce8a-120">-PartnerServerName</span></span>
<span data-ttu-id="8ce8a-121">Especifica o nome do servidor de banco de dados SQL do Azure atuar como secundário.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-121">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce8a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce8a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ce8a-123">Especifica o nome do grupo de recursos do Azure ao qual esse cmdlet atribui o banco de dados primário.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="8ce8a-124">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8ce8a-124">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="8ce8a-125">Especifica o nome do pool elástico no qual colocar o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-125">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce8a-126">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="8ce8a-126">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="8ce8a-127">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-127">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce8a-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="8ce8a-128">-ServerName</span></span>
<span data-ttu-id="8ce8a-129">Especifica o nome do SQL Server do banco de dados SQL primário.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-129">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="8ce8a-130">-Marcas</span><span class="sxs-lookup"><span data-stu-id="8ce8a-130">-Tags</span></span>
<span data-ttu-id="8ce8a-131">Especifica os pares de valores chave na forma de uma tabela de hash a serem associados ao link de replicação do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-131">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="8ce8a-132">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8ce8a-132">For example:</span></span>

<span data-ttu-id="8ce8a-133">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8ce8a-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ce8a-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ce8a-134">-Confirm</span></span>
<span data-ttu-id="8ce8a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce8a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce8a-136">-WhatIf</span></span>
<span data-ttu-id="8ce8a-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ce8a-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce8a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce8a-139">-DefaultProfile</span></span>
<span data-ttu-id="8ce8a-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ce8a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce8a-141">CommonParameters</span></span>
<span data-ttu-id="8ce8a-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ce8a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce8a-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce8a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce8a-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ce8a-144">INPUTS</span></span>

## <span data-ttu-id="8ce8a-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ce8a-145">OUTPUTS</span></span>

### <span data-ttu-id="8ce8a-146">Microsoft. Azure. Commands. Sql. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="8ce8a-146">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="8ce8a-147">Esse cmdlet retorna objetos **ReplicationLink** .</span><span class="sxs-lookup"><span data-stu-id="8ce8a-147">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="8ce8a-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ce8a-148">NOTES</span></span>

## <span data-ttu-id="8ce8a-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ce8a-149">RELATED LINKS</span></span>

[<span data-ttu-id="8ce8a-150">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8ce8a-150">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="8ce8a-151">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8ce8a-151">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="8ce8a-152">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="8ce8a-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
