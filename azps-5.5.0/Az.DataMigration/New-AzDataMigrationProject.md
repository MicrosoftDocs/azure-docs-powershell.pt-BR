---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116859"
---
# <span data-ttu-id="2b97b-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2b97b-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="2b97b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b97b-102">SYNOPSIS</span></span>
<span data-ttu-id="2b97b-103">Cria um novo projeto do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b97b-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="2b97b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b97b-104">SYNTAX</span></span>

### <span data-ttu-id="2b97b-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b97b-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b97b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b97b-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b97b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b97b-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b97b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b97b-108">DESCRIPTION</span></span>
<span data-ttu-id="2b97b-109">O New-AzDataMigrationProject cmdlet cria um novo projeto do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b97b-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="2b97b-110">Esse cmdlet assume todos os parâmetros necessários, como o nome do Grupo de Recursos do Azure, o nome do Serviço de Migração de Dados do Azure na qual o novo projeto deve ser criado, a região na qual o projeto deve ser criado, o nome exclusivo do novo projeto, os objetos de conexão de origem e de destino e o objeto do tipo de destino, como entrada para a lista de bancos de dados a serem migrados.</span><span class="sxs-lookup"><span data-stu-id="2b97b-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="2b97b-111">Use o cmdlet New-AzDataMigrationConnectionInfo para criar um novo objeto ConnectionInfo para as conexões de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="2b97b-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="2b97b-112">A lista de Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo é esperada para bancos de dados selecionados; esse objeto pode ser criado usando New-AzDataMigrationDatabaseInfo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b97b-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="2b97b-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2b97b-113">EXAMPLES</span></span>

### <span data-ttu-id="2b97b-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b97b-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="2b97b-115">O exemplo acima mostra como criar um novo projeto chamado MyDMSProject localizado na região central dos EUA sob a instância do Serviço de Migração de Banco de Dados do Azure chamada TestService.</span><span class="sxs-lookup"><span data-stu-id="2b97b-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="2b97b-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b97b-116">PARAMETERS</span></span>

### <span data-ttu-id="2b97b-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="2b97b-117">-DatabaseInfo</span></span>
<span data-ttu-id="2b97b-118">Informações do Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="2b97b-118">Database Infos.</span></span>

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

### <span data-ttu-id="2b97b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b97b-119">-DefaultProfile</span></span>
<span data-ttu-id="2b97b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b97b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b97b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b97b-121">-InputObject</span></span>
<span data-ttu-id="2b97b-122">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="2b97b-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="2b97b-123">-Local</span><span class="sxs-lookup"><span data-stu-id="2b97b-123">-Location</span></span>
<span data-ttu-id="2b97b-124">O local da instância do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b97b-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="2b97b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b97b-125">-Name</span></span>
<span data-ttu-id="2b97b-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="2b97b-126">The name of the project.</span></span>

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

### <span data-ttu-id="2b97b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b97b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2b97b-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b97b-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b97b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b97b-129">-ResourceId</span></span>
<span data-ttu-id="2b97b-130">ID do Recurso DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="2b97b-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="2b97b-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2b97b-131">-ServiceName</span></span>
<span data-ttu-id="2b97b-132">O nome da instância do Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b97b-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="2b97b-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="2b97b-133">-SourceConnection</span></span>
<span data-ttu-id="2b97b-134">Informações de conexão de origem.</span><span class="sxs-lookup"><span data-stu-id="2b97b-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="2b97b-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="2b97b-135">-SourceType</span></span>
<span data-ttu-id="2b97b-136">Tipo de plataforma de origem para o projeto.</span><span class="sxs-lookup"><span data-stu-id="2b97b-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="2b97b-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="2b97b-137">-TargetConnection</span></span>
<span data-ttu-id="2b97b-138">Informações de conexão de destino.</span><span class="sxs-lookup"><span data-stu-id="2b97b-138">Target connection information.</span></span>

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

### <span data-ttu-id="2b97b-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="2b97b-139">-TargetType</span></span>
<span data-ttu-id="2b97b-140">Tipo de plataforma de destino para o projeto.</span><span class="sxs-lookup"><span data-stu-id="2b97b-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="2b97b-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2b97b-141">-Confirm</span></span>
<span data-ttu-id="2b97b-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b97b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b97b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b97b-143">-WhatIf</span></span>
<span data-ttu-id="2b97b-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2b97b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b97b-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b97b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b97b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b97b-146">CommonParameters</span></span>
<span data-ttu-id="2b97b-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b97b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b97b-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b97b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b97b-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="2b97b-149">INPUTS</span></span>

### <span data-ttu-id="2b97b-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2b97b-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="2b97b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="2b97b-151">System.String</span></span>

## <span data-ttu-id="2b97b-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="2b97b-152">OUTPUTS</span></span>

### <span data-ttu-id="2b97b-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="2b97b-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="2b97b-154">Notas</span><span class="sxs-lookup"><span data-stu-id="2b97b-154">NOTES</span></span>

## <span data-ttu-id="2b97b-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b97b-155">RELATED LINKS</span></span>
