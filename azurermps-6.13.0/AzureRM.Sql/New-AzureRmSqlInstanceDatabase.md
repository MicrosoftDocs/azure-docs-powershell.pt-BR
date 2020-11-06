---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 2ef6ff642d22429ae22186ce01a4a17dad125b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430827"
---
# <span data-ttu-id="80220-101">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="80220-101">New-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="80220-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80220-102">SYNOPSIS</span></span>
<span data-ttu-id="80220-103">Cria um banco de dados de instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="80220-103">Creates an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80220-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80220-104">SYNTAX</span></span>

### <span data-ttu-id="80220-105">CreateNewInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="80220-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80220-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="80220-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80220-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="80220-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80220-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80220-108">DESCRIPTION</span></span>
<span data-ttu-id="80220-109">O cmdlet **New-AzureRmSqlInstanceDatabase** cria um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="80220-109">The **New-AzureRmSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="80220-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80220-110">EXAMPLES</span></span>

### <span data-ttu-id="80220-111">Exemplo 1: criar um banco de dados em uma instância especificada</span><span class="sxs-lookup"><span data-stu-id="80220-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="80220-112">Esse comando cria um banco de dados de instância denominado Database01 na instância managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="80220-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="80220-113">OS</span><span class="sxs-lookup"><span data-stu-id="80220-113">PARAMETERS</span></span>

### <span data-ttu-id="80220-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80220-114">-AsJob</span></span>
<span data-ttu-id="80220-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="80220-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80220-116">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="80220-116">-Collation</span></span>
<span data-ttu-id="80220-117">O agrupamento do agrupamento do banco de dados de instância SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="80220-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80220-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80220-118">-DefaultProfile</span></span>
<span data-ttu-id="80220-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80220-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80220-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="80220-120">-InstanceName</span></span>
<span data-ttu-id="80220-121">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="80220-121">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80220-122">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="80220-122">-InstanceObject</span></span>
<span data-ttu-id="80220-123">O objeto de instância</span><span class="sxs-lookup"><span data-stu-id="80220-123">The instance object</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80220-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="80220-124">-InstanceResourceId</span></span>
<span data-ttu-id="80220-125">A ID do recurso da instância</span><span class="sxs-lookup"><span data-stu-id="80220-125">The instance resource id</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80220-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="80220-126">-Name</span></span>
<span data-ttu-id="80220-127">O nome do banco de dados de instância SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="80220-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80220-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80220-128">-ResourceGroupName</span></span>
<span data-ttu-id="80220-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="80220-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80220-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="80220-130">-Tag</span></span>
<span data-ttu-id="80220-131">As marcas a serem associadas ao banco de dados de instância SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="80220-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80220-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="80220-132">-Confirm</span></span>
<span data-ttu-id="80220-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80220-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80220-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80220-134">-WhatIf</span></span>
<span data-ttu-id="80220-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80220-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80220-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80220-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80220-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80220-137">CommonParameters</span></span>
<span data-ttu-id="80220-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80220-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80220-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80220-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80220-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80220-140">INPUTS</span></span>

### <span data-ttu-id="80220-141">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="80220-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="80220-142">System. String</span><span class="sxs-lookup"><span data-stu-id="80220-142">System.String</span></span>

## <span data-ttu-id="80220-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80220-143">OUTPUTS</span></span>

### <span data-ttu-id="80220-144">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="80220-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="80220-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80220-145">NOTES</span></span>

## <span data-ttu-id="80220-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80220-146">RELATED LINKS</span></span>
