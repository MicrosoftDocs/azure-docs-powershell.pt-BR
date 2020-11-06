---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 3d36c94ebcc1b733559f9fb4075fb20e4ec67144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602677"
---
# <span data-ttu-id="f03aa-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f03aa-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f03aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f03aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f03aa-103">Define propriedades para um banco de dados ou move um banco de dados existente para um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f03aa-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f03aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f03aa-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f03aa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f03aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f03aa-106">O cmdlet **set-AzureRmSqlDatabase** define propriedades para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f03aa-106">The **Set-AzureRmSqlDatabase** cmdlet sets properties for an Azure SQL database.</span></span>
<span data-ttu-id="f03aa-107">Além disso, você pode especificar o parâmetro *ElasticPoolName* para mover um banco de dados para um pool elástico.</span><span class="sxs-lookup"><span data-stu-id="f03aa-107">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span>
<span data-ttu-id="f03aa-108">Se um banco de dados já estiver em um pool elástico, você pode usar o parâmetro *RequestedServiceObjectiveName* para atribuir um nível de desempenho.</span><span class="sxs-lookup"><span data-stu-id="f03aa-108">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to assign a performance level.</span></span>

## <span data-ttu-id="f03aa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f03aa-109">EXAMPLES</span></span>

### <span data-ttu-id="f03aa-110">Exemplo 1: atualizar um banco de dados em um banco de dados S2 padrão</span><span class="sxs-lookup"><span data-stu-id="f03aa-110">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="f03aa-111">Esse comando atualiza um banco de dados denominado Database01 para um banco de dados S2 padrão em um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="f03aa-111">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="f03aa-112">Exemplo 2: adicionar um banco de dados a um pool elástico</span><span class="sxs-lookup"><span data-stu-id="f03aa-112">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="f03aa-113">Esse comando adiciona um banco de dados denominado Database01 ao pool elástico chamado ElasticPool01 hospedado no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="f03aa-113">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

## <span data-ttu-id="f03aa-114">OS</span><span class="sxs-lookup"><span data-stu-id="f03aa-114">PARAMETERS</span></span>

### <span data-ttu-id="f03aa-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f03aa-115">-DatabaseName</span></span>
<span data-ttu-id="f03aa-116">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f03aa-116">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f03aa-117">-Edição</span><span class="sxs-lookup"><span data-stu-id="f03aa-117">-Edition</span></span>
<span data-ttu-id="f03aa-118">Especifica a edição para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f03aa-118">Specifies the edition for the database.</span></span>
<span data-ttu-id="f03aa-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f03aa-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f03aa-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f03aa-120">None</span></span>
- <span data-ttu-id="f03aa-121">Gratifica</span><span class="sxs-lookup"><span data-stu-id="f03aa-121">Premium</span></span>
- <span data-ttu-id="f03aa-122">Basic</span><span class="sxs-lookup"><span data-stu-id="f03aa-122">Basic</span></span>
- <span data-ttu-id="f03aa-123">Oficial</span><span class="sxs-lookup"><span data-stu-id="f03aa-123">Standard</span></span>
- <span data-ttu-id="f03aa-124">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="f03aa-124">DataWarehouse</span></span>
- <span data-ttu-id="f03aa-125">Gratuito</span><span class="sxs-lookup"><span data-stu-id="f03aa-125">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f03aa-126">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f03aa-126">-ElasticPoolName</span></span>
<span data-ttu-id="f03aa-127">Especifica o nome do pool elástico no qual mover o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f03aa-127">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="f03aa-128">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="f03aa-128">-MaxSizeBytes</span></span>
<span data-ttu-id="f03aa-129">Especifica o novo tamanho máximo para o banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="f03aa-129">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="f03aa-130">Você pode especificar o parâmetro ou o *MaxSizeGB*.</span><span class="sxs-lookup"><span data-stu-id="f03aa-130">You can specify either this parameter or *MaxSizeGB*.</span></span>
<span data-ttu-id="f03aa-131">Consulte o parâmetro *MaxSizeGB* para obter valores aceitáveis por edição.</span><span class="sxs-lookup"><span data-stu-id="f03aa-131">See the *MaxSizeGB* parameter for acceptable values per edition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f03aa-132">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="f03aa-132">-ReadScale</span></span>
<span data-ttu-id="f03aa-133">A opção de escala de leitura para atribuir ao banco de dados SQL do Azure. (Habilitado/desabilitado)</span><span class="sxs-lookup"><span data-stu-id="f03aa-133">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f03aa-134">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f03aa-134">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="f03aa-135">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f03aa-135">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="f03aa-136">Para obter informações sobre os objetivos do serviço, consulte [níveis de desempenho e camadas do serviço de banco de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) na biblioteca do Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="f03aa-136">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="f03aa-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03aa-137">-ResourceGroupName</span></span>
<span data-ttu-id="f03aa-138">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f03aa-138">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f03aa-139">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f03aa-139">-ServerName</span></span>
<span data-ttu-id="f03aa-140">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f03aa-140">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="f03aa-141">-Marcas</span><span class="sxs-lookup"><span data-stu-id="f03aa-141">-Tags</span></span>
<span data-ttu-id="f03aa-142">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f03aa-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f03aa-143">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f03aa-143">For example:</span></span>

<span data-ttu-id="f03aa-144">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f03aa-144">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f03aa-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f03aa-145">-Confirm</span></span>
<span data-ttu-id="f03aa-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f03aa-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f03aa-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f03aa-147">-WhatIf</span></span>
<span data-ttu-id="f03aa-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f03aa-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f03aa-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f03aa-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f03aa-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03aa-150">-DefaultProfile</span></span>
<span data-ttu-id="f03aa-151">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f03aa-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f03aa-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03aa-152">CommonParameters</span></span>
<span data-ttu-id="f03aa-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f03aa-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03aa-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f03aa-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03aa-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f03aa-155">INPUTS</span></span>

## <span data-ttu-id="f03aa-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f03aa-156">OUTPUTS</span></span>

### <span data-ttu-id="f03aa-157">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f03aa-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f03aa-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f03aa-158">NOTES</span></span>

## <span data-ttu-id="f03aa-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f03aa-159">RELATED LINKS</span></span>

[<span data-ttu-id="f03aa-160">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f03aa-160">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="f03aa-161">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f03aa-161">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="f03aa-162">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f03aa-162">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="f03aa-163">Currículo-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f03aa-163">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="f03aa-164">Suspender-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f03aa-164">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="f03aa-165">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f03aa-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
