---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 99884c23ff99287deb721e3cb76871766cdfa7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440468"
---
# <span data-ttu-id="43769-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="43769-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="43769-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43769-102">SYNOPSIS</span></span>
<span data-ttu-id="43769-103">Cria um novo projeto do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="43769-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43769-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43769-104">SYNTAX</span></span>

### <span data-ttu-id="43769-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="43769-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform>
 [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="43769-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43769-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="43769-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43769-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="43769-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43769-108">DESCRIPTION</span></span>
<span data-ttu-id="43769-109">O cmdlet New-AzureRmDataMigrationProject cria um novo projeto do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="43769-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="43769-110">Esse cmdlet assume todos os parâmetros necessários, como o nome do grupo de recursos do Azure, o nome do serviço de migração de dados do Azure no qual o novo projeto deve ser criado, a região em que o projeto deve ser criado, o nome exclusivo do novo projeto, os objetos de conexão de origem e de destino e o objeto de tipo de destino, como entrada para a lista de bancos de dados</span><span class="sxs-lookup"><span data-stu-id="43769-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="43769-111">Use o cmdlet New-AzureRmDataMigrationConnectionInfo para criar um novo objeto ConnectionInfo para as conexões de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="43769-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="43769-112">A lista de Microsoft. Azure. Management. datamigration. Models. DatabaseInfo é esperada para bancos de dados selecionados; esse objeto pode ser criado usando-se New-AzureRmDataMigrationDatabaseInfo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43769-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="43769-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43769-113">EXAMPLES</span></span>

### <span data-ttu-id="43769-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43769-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="43769-115">O exemplo acima mostra como criar um novo projeto chamado MyDMSProject localizado na região central dos EUA na instância do serviço de migração de banco de dados do Azure chamada TestService.</span><span class="sxs-lookup"><span data-stu-id="43769-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>



## <span data-ttu-id="43769-116">OS</span><span class="sxs-lookup"><span data-stu-id="43769-116">PARAMETERS</span></span>

### <span data-ttu-id="43769-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="43769-117">-Confirm</span></span>
<span data-ttu-id="43769-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43769-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43769-119">-DatabaseInfo[]</span><span class="sxs-lookup"><span data-stu-id="43769-119">-DatabaseInfo[]</span></span>
<span data-ttu-id="43769-120">Informações do banco de dados</span><span class="sxs-lookup"><span data-stu-id="43769-120">Database information</span></span>

```yaml
Type: DatabaseInfo[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43769-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43769-121">-DefaultProfile</span></span>
<span data-ttu-id="43769-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43769-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43769-123">-Local</span><span class="sxs-lookup"><span data-stu-id="43769-123">-Location</span></span>
<span data-ttu-id="43769-124">O local da instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="43769-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43769-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="43769-125">-ProjectName</span></span>
<span data-ttu-id="43769-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="43769-126">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43769-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43769-127">-ResourceGroupName</span></span>
<span data-ttu-id="43769-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="43769-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43769-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="43769-129">-ServiceName</span></span>
<span data-ttu-id="43769-130">O nome da instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="43769-130">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43769-131">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="43769-131">-SourceConnection</span></span>
<span data-ttu-id="43769-132">Informações de conexão de origem.</span><span class="sxs-lookup"><span data-stu-id="43769-132">Source Connection Info.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43769-133">-SourceType</span><span class="sxs-lookup"><span data-stu-id="43769-133">-SourceType</span></span>
<span data-ttu-id="43769-134">Tipo de plataforma de origem para o Project.</span><span class="sxs-lookup"><span data-stu-id="43769-134">Source platform type for project.</span></span>

```yaml
Type: ProjectSourcePlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43769-135">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="43769-135">-TargetConnection</span></span>
<span data-ttu-id="43769-136">Informações de conexão de destino.</span><span class="sxs-lookup"><span data-stu-id="43769-136">Target connection information.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43769-137">-TargetType</span><span class="sxs-lookup"><span data-stu-id="43769-137">-TargetType</span></span>
<span data-ttu-id="43769-138">Tipo de plataforma de destino do Project.</span><span class="sxs-lookup"><span data-stu-id="43769-138">Target platform type for project.</span></span>

```yaml
Type: ProjectTargetPlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="43769-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43769-139">OUTPUTS</span></span>

### <span data-ttu-id="43769-140">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="43769-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>


## <span data-ttu-id="43769-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43769-141">NOTES</span></span>

## <span data-ttu-id="43769-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43769-142">RELATED LINKS</span></span>

