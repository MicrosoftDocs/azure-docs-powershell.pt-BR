---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116143"
---
# <span data-ttu-id="d2fc0-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d2fc0-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="d2fc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d2fc0-103">Cria um banco de dados de Instância Gerenciada do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="d2fc0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2fc0-104">SYNTAX</span></span>

### <span data-ttu-id="d2fc0-105">CreateNewInstanceDatabaseFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2fc0-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2fc0-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d2fc0-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2fc0-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d2fc0-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2fc0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2fc0-108">DESCRIPTION</span></span>
<span data-ttu-id="d2fc0-109">O **cmdlet New-AzSqlInstanceDatabase** cria um banco de dados de instância sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="d2fc0-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2fc0-110">EXAMPLES</span></span>

### <span data-ttu-id="d2fc0-111">Exemplo 1: Criar um banco de dados em uma instância especificada</span><span class="sxs-lookup"><span data-stu-id="d2fc0-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="d2fc0-112">Esse comando cria um banco de dados de instância chamado Database01 na instância managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="d2fc0-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2fc0-113">PARAMETERS</span></span>

### <span data-ttu-id="d2fc0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2fc0-114">-AsJob</span></span>
<span data-ttu-id="d2fc0-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d2fc0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2fc0-116">-Colagem</span><span class="sxs-lookup"><span data-stu-id="d2fc0-116">-Collation</span></span>
<span data-ttu-id="d2fc0-117">O colamento do banco de dados de instância SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="d2fc0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2fc0-118">-DefaultProfile</span></span>
<span data-ttu-id="d2fc0-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2fc0-120">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="d2fc0-120">-InstanceName</span></span>
<span data-ttu-id="d2fc0-121">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2fc0-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="d2fc0-122">-InstanceObject</span></span>
<span data-ttu-id="d2fc0-123">O objeto de instância</span><span class="sxs-lookup"><span data-stu-id="d2fc0-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2fc0-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d2fc0-124">-InstanceResourceId</span></span>
<span data-ttu-id="d2fc0-125">A ID do recurso de instância</span><span class="sxs-lookup"><span data-stu-id="d2fc0-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2fc0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2fc0-126">-Name</span></span>
<span data-ttu-id="d2fc0-127">O nome do Banco de Dados de Instância SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2fc0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2fc0-128">-ResourceGroupName</span></span>
<span data-ttu-id="d2fc0-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2fc0-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2fc0-130">-Tag</span></span>
<span data-ttu-id="d2fc0-131">As marcas a associar ao Banco de Dados de Instância sql do Azure</span><span class="sxs-lookup"><span data-stu-id="d2fc0-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2fc0-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d2fc0-132">-Confirm</span></span>
<span data-ttu-id="d2fc0-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2fc0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2fc0-134">-WhatIf</span></span>
<span data-ttu-id="d2fc0-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2fc0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2fc0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2fc0-137">CommonParameters</span></span>
<span data-ttu-id="d2fc0-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2fc0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2fc0-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2fc0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2fc0-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="d2fc0-140">INPUTS</span></span>

### <span data-ttu-id="d2fc0-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d2fc0-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d2fc0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d2fc0-142">System.String</span></span>

## <span data-ttu-id="d2fc0-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="d2fc0-143">OUTPUTS</span></span>

### <span data-ttu-id="d2fc0-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d2fc0-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d2fc0-145">Notas</span><span class="sxs-lookup"><span data-stu-id="d2fc0-145">NOTES</span></span>

## <span data-ttu-id="d2fc0-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2fc0-146">RELATED LINKS</span></span>
