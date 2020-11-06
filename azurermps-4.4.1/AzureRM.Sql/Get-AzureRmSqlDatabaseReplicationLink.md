---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 05b090de647f1c6e6abfb7f2c83e5bd0a4cf616b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432999"
---
# <span data-ttu-id="89255-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="89255-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="89255-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89255-102">SYNOPSIS</span></span>
<span data-ttu-id="89255-103">Obtém os links de replicação geográfica entre um banco de dados SQL do Azure e um grupo de recursos ou um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="89255-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89255-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89255-104">SYNTAX</span></span>

### <span data-ttu-id="89255-105">ByDatabaseName (padrão)</span><span class="sxs-lookup"><span data-stu-id="89255-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89255-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="89255-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89255-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89255-107">DESCRIPTION</span></span>
<span data-ttu-id="89255-108">O cmdlet **Get-AzureRMSqlDatabaseReplicationLink** substitui o cmdlet **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="89255-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="89255-109">Ele obtém todos os links de replicação geográfica entre o banco de dados SQL do Azure especificado e um grupo de recursos ou AzureSQL Server.</span><span class="sxs-lookup"><span data-stu-id="89255-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="89255-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89255-110">EXAMPLES</span></span>

## <span data-ttu-id="89255-111">OS</span><span class="sxs-lookup"><span data-stu-id="89255-111">PARAMETERS</span></span>

### <span data-ttu-id="89255-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="89255-112">-DatabaseName</span></span>
<span data-ttu-id="89255-113">Especifica o nome do banco de dados SQL para o qual recuperar links.</span><span class="sxs-lookup"><span data-stu-id="89255-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="89255-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89255-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="89255-115">Especifica o nome do grupo de recursos ao qual o parceiro está atribuído.</span><span class="sxs-lookup"><span data-stu-id="89255-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="89255-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="89255-116">-PartnerServerName</span></span>
<span data-ttu-id="89255-117">Especifica o nome do Azure SQL Server para o parceiro.</span><span class="sxs-lookup"><span data-stu-id="89255-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPartnerServerName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89255-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89255-118">-ResourceGroupName</span></span>
<span data-ttu-id="89255-119">Especifica o nome do grupo de recursos do Azure para o banco de dados para o qual recuperar links.</span><span class="sxs-lookup"><span data-stu-id="89255-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="89255-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="89255-120">-ServerName</span></span>
<span data-ttu-id="89255-121">Especifica o nome do SQL Server para o banco de dados para o qual recuperar links.</span><span class="sxs-lookup"><span data-stu-id="89255-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="89255-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89255-122">-Confirm</span></span>
<span data-ttu-id="89255-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89255-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89255-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89255-124">-WhatIf</span></span>
<span data-ttu-id="89255-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89255-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89255-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89255-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89255-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89255-127">-DefaultProfile</span></span>
<span data-ttu-id="89255-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89255-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89255-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89255-129">CommonParameters</span></span>
<span data-ttu-id="89255-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89255-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89255-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89255-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89255-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89255-132">INPUTS</span></span>

###  
<span data-ttu-id="89255-133">Esse cmdlet aceita instâncias do **ReplicationLink** ou do objeto de **banco de dados** para o banco de dados primário ou secundário.</span><span class="sxs-lookup"><span data-stu-id="89255-133">This cmdlet accepts instances of the **ReplicationLink** or the **Database** object for the primary or secondary database.</span></span>

## <span data-ttu-id="89255-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89255-134">OUTPUTS</span></span>

###  
<span data-ttu-id="89255-135">Esse cmdlet retorna um objeto **ReplicationLink** .</span><span class="sxs-lookup"><span data-stu-id="89255-135">This cmdlet returns a **ReplicationLink** object.</span></span>

## <span data-ttu-id="89255-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89255-136">NOTES</span></span>

## <span data-ttu-id="89255-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89255-137">RELATED LINKS</span></span>

[<span data-ttu-id="89255-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="89255-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
