---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: a190e6a47c0a3027505c471be870c10ac80593cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112546"
---
# <span data-ttu-id="66c3d-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="66c3d-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="66c3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="66c3d-103">Obtém as operações de uma instância gerenciada pelo SQL.</span><span class="sxs-lookup"><span data-stu-id="66c3d-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="66c3d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66c3d-104">SYNTAX</span></span>

### <span data-ttu-id="66c3d-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="66c3d-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c3d-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="66c3d-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66c3d-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="66c3d-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66c3d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="66c3d-108">DESCRIPTION</span></span>
<span data-ttu-id="66c3d-109">O Get-AzSqlInstanceOperation cmdlet obtém informações sobre as operações em uma instância gerenciada pelo SQL.</span><span class="sxs-lookup"><span data-stu-id="66c3d-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="66c3d-110">Você pode exibir todas as operações em uma instância gerenciada ou exibir uma operação específica fornecendo o nome da operação.</span><span class="sxs-lookup"><span data-stu-id="66c3d-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="66c3d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66c3d-111">EXAMPLES</span></span>

### <span data-ttu-id="66c3d-112">Exemplo 1: Obter todas as operações da instância</span><span class="sxs-lookup"><span data-stu-id="66c3d-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="66c3d-113">Esse comando obtém todas as operações de uma instância gerenciada pelo SQL.</span><span class="sxs-lookup"><span data-stu-id="66c3d-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="66c3d-114">Exemplo 2: Obter uma operação específica</span><span class="sxs-lookup"><span data-stu-id="66c3d-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="66c3d-115">Este comando obtém a operação com o nome '5870c6d8-6703-4b27-8ae4-687b4ca7caea' em uma instância gerenciada pelo SQL.</span><span class="sxs-lookup"><span data-stu-id="66c3d-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="66c3d-116">Exemplo 3: Usando a ID do recurso de operação</span><span class="sxs-lookup"><span data-stu-id="66c3d-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="66c3d-117">Este comando obtém a operação com id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span><span class="sxs-lookup"><span data-stu-id="66c3d-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="66c3d-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66c3d-118">PARAMETERS</span></span>

### <span data-ttu-id="66c3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c3d-119">-DefaultProfile</span></span>
<span data-ttu-id="66c3d-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66c3d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66c3d-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="66c3d-121">-ManagedInstanceName</span></span>
<span data-ttu-id="66c3d-122">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="66c3d-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c3d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="66c3d-123">-Name</span></span>
<span data-ttu-id="66c3d-124">O nome da operação.</span><span class="sxs-lookup"><span data-stu-id="66c3d-124">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c3d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c3d-125">-ResourceGroupName</span></span>
<span data-ttu-id="66c3d-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66c3d-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c3d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66c3d-127">-ResourceId</span></span>
<span data-ttu-id="66c3d-128">O identificador de recurso de operação de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="66c3d-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c3d-129">CommonParameters</span></span>
<span data-ttu-id="66c3d-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c3d-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66c3d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c3d-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="66c3d-132">INPUTS</span></span>

### <span data-ttu-id="66c3d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="66c3d-133">System.String</span></span>

## <span data-ttu-id="66c3d-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="66c3d-134">OUTPUTS</span></span>

### <span data-ttu-id="66c3d-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="66c3d-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="66c3d-136">Notas</span><span class="sxs-lookup"><span data-stu-id="66c3d-136">NOTES</span></span>

## <span data-ttu-id="66c3d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66c3d-137">RELATED LINKS</span></span>
