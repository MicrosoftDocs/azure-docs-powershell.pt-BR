---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: 5b1817ef0924f4e7bb1c07152b9adc47cc27292f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885778"
---
# <span data-ttu-id="86ea9-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="86ea9-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="86ea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="86ea9-103">Remove um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="86ea9-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="86ea9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="86ea9-104">SYNTAX</span></span>

### <span data-ttu-id="86ea9-105">RemoveInstanceDatabaseFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="86ea9-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ea9-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="86ea9-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ea9-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="86ea9-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86ea9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="86ea9-108">DESCRIPTION</span></span>
<span data-ttu-id="86ea9-109">O cmdlet **Remove-AzSqlInstanceDatabase** remove um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="86ea9-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="86ea9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86ea9-110">EXAMPLES</span></span>

### <span data-ttu-id="86ea9-111">Exemplo 1: Remover um banco de dados de uma instância</span><span class="sxs-lookup"><span data-stu-id="86ea9-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="86ea9-112">Este comando remove o banco de dados chamado Database01 da instância managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="86ea9-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="86ea9-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="86ea9-113">PARAMETERS</span></span>

### <span data-ttu-id="86ea9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ea9-114">-DefaultProfile</span></span>
<span data-ttu-id="86ea9-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86ea9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86ea9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="86ea9-116">-Force</span></span>
<span data-ttu-id="86ea9-117">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="86ea9-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="86ea9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86ea9-118">-InputObject</span></span>
<span data-ttu-id="86ea9-119">O objeto Instance Database a ser removido</span><span class="sxs-lookup"><span data-stu-id="86ea9-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86ea9-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="86ea9-120">-InstanceName</span></span>
<span data-ttu-id="86ea9-121">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="86ea9-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ea9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="86ea9-122">-Name</span></span>
<span data-ttu-id="86ea9-123">O nome do Banco de Dados de Instância SQL Azure a ser removido.</span><span class="sxs-lookup"><span data-stu-id="86ea9-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ea9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ea9-124">-ResourceGroupName</span></span>
<span data-ttu-id="86ea9-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="86ea9-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ea9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86ea9-126">-ResourceId</span></span>
<span data-ttu-id="86ea9-127">A id de recurso do objeto Banco de Dados de Instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="86ea9-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ea9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86ea9-128">-Confirm</span></span>
<span data-ttu-id="86ea9-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86ea9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ea9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ea9-130">-WhatIf</span></span>
<span data-ttu-id="86ea9-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="86ea9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86ea9-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="86ea9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ea9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ea9-133">CommonParameters</span></span>
<span data-ttu-id="86ea9-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ea9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ea9-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86ea9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ea9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86ea9-136">INPUTS</span></span>

### <span data-ttu-id="86ea9-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="86ea9-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="86ea9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="86ea9-138">System.String</span></span>

## <span data-ttu-id="86ea9-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="86ea9-139">OUTPUTS</span></span>

### <span data-ttu-id="86ea9-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="86ea9-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="86ea9-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="86ea9-141">NOTES</span></span>

## <span data-ttu-id="86ea9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86ea9-142">RELATED LINKS</span></span>
