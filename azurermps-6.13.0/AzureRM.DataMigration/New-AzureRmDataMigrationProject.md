---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 9abb97e5006f6572c7a0b08d8d25bcc55906a765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430311"
---
# <span data-ttu-id="2330f-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2330f-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="2330f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2330f-102">SYNOPSIS</span></span>
<span data-ttu-id="2330f-103">Cria um novo projeto do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2330f-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2330f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2330f-104">SYNTAX</span></span>

### <span data-ttu-id="2330f-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2330f-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2330f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2330f-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2330f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2330f-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2330f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2330f-108">DESCRIPTION</span></span>
<span data-ttu-id="2330f-109">O cmdlet New-AzureRmDataMigrationProject cria um novo projeto do serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2330f-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="2330f-110">Esse cmdlet assume todos os parâmetros necessários, como o nome do grupo de recursos do Azure, o nome do serviço de migração de dados do Azure no qual o novo projeto deve ser criado, a região em que o projeto deve ser criado, o nome exclusivo do novo projeto, os objetos de conexão de origem e de destino e o objeto de tipo de destino, como entrada para a lista de bancos de dados</span><span class="sxs-lookup"><span data-stu-id="2330f-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="2330f-111">Use o cmdlet New-AzureRmDataMigrationConnectionInfo para criar um novo objeto ConnectionInfo para as conexões de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="2330f-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="2330f-112">A lista de Microsoft. Azure. Management. datamigration. Models. DatabaseInfo é esperada para bancos de dados selecionados; esse objeto pode ser criado usando-se New-AzureRmDataMigrationDatabaseInfo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2330f-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="2330f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2330f-113">EXAMPLES</span></span>

### <span data-ttu-id="2330f-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2330f-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="2330f-115">O exemplo acima mostra como criar um novo projeto chamado MyDMSProject localizado na região central dos EUA na instância do serviço de migração de banco de dados do Azure chamada TestService.</span><span class="sxs-lookup"><span data-stu-id="2330f-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="2330f-116">OS</span><span class="sxs-lookup"><span data-stu-id="2330f-116">PARAMETERS</span></span>

### <span data-ttu-id="2330f-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="2330f-117">-DatabaseInfo</span></span>
<span data-ttu-id="2330f-118">Informações de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2330f-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2330f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2330f-119">-DefaultProfile</span></span>
<span data-ttu-id="2330f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2330f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2330f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2330f-121">-InputObject</span></span>
<span data-ttu-id="2330f-122">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="2330f-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2330f-123">-Local</span><span class="sxs-lookup"><span data-stu-id="2330f-123">-Location</span></span>
<span data-ttu-id="2330f-124">O local da instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2330f-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="2330f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2330f-125">-Name</span></span>
<span data-ttu-id="2330f-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="2330f-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2330f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2330f-127">-ResourceGroupName</span></span>
<span data-ttu-id="2330f-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2330f-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2330f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2330f-129">-ResourceId</span></span>
<span data-ttu-id="2330f-130">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="2330f-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2330f-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2330f-131">-ServiceName</span></span>
<span data-ttu-id="2330f-132">O nome da instância do serviço de migração do banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2330f-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2330f-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="2330f-133">-SourceConnection</span></span>
<span data-ttu-id="2330f-134">Informações de conexão de origem.</span><span class="sxs-lookup"><span data-stu-id="2330f-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2330f-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="2330f-135">-SourceType</span></span>
<span data-ttu-id="2330f-136">Tipo de plataforma de origem para o Project.</span><span class="sxs-lookup"><span data-stu-id="2330f-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="2330f-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="2330f-137">-TargetConnection</span></span>
<span data-ttu-id="2330f-138">Informações de conexão de destino.</span><span class="sxs-lookup"><span data-stu-id="2330f-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2330f-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="2330f-139">-TargetType</span></span>
<span data-ttu-id="2330f-140">Tipo de plataforma de destino do Project.</span><span class="sxs-lookup"><span data-stu-id="2330f-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="2330f-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2330f-141">-Confirm</span></span>
<span data-ttu-id="2330f-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2330f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2330f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2330f-143">-WhatIf</span></span>
<span data-ttu-id="2330f-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2330f-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2330f-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2330f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2330f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2330f-146">CommonParameters</span></span>
<span data-ttu-id="2330f-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2330f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2330f-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2330f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2330f-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2330f-149">INPUTS</span></span>

### <span data-ttu-id="2330f-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2330f-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="2330f-151">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2330f-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2330f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2330f-152">System.String</span></span>

## <span data-ttu-id="2330f-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2330f-153">OUTPUTS</span></span>

### <span data-ttu-id="2330f-154">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="2330f-154">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="2330f-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2330f-155">NOTES</span></span>

## <span data-ttu-id="2330f-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2330f-156">RELATED LINKS</span></span>
