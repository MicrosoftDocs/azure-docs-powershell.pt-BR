---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: b9f008d610729d1f1bc73affbb5b8f3eae04ecdd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944259"
---
# <span data-ttu-id="1eb8e-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="1eb8e-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="1eb8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1eb8e-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb8e-103">Obtém as operações de uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="1eb8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1eb8e-104">SYNTAX</span></span>

### <span data-ttu-id="1eb8e-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1eb8e-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <Guid>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb8e-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb8e-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1eb8e-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb8e-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eb8e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1eb8e-108">DESCRIPTION</span></span>
<span data-ttu-id="1eb8e-109">O cmdlet Get-AzSqlInstanceOperation Obtém informações sobre as operações em uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="1eb8e-110">Você pode exibir todas as operações em uma instância gerenciada ou exibir uma operação específica fornecendo o nome da operação.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="1eb8e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1eb8e-111">EXAMPLES</span></span>

### <span data-ttu-id="1eb8e-112">Exemplo 1: obter as operações de todas as instâncias</span><span class="sxs-lookup"><span data-stu-id="1eb8e-112">Example 1: Get all instance's operations</span></span>
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
```

<span data-ttu-id="1eb8e-113">Esse comando obtém todas as operações em uma instância gerenciada pelo SQL.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="1eb8e-114">Exemplo 2: obter uma operação específica</span><span class="sxs-lookup"><span data-stu-id="1eb8e-114">Example 2: Get a specific operation</span></span>
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
```

<span data-ttu-id="1eb8e-115">Este comando obtém a operação com o nome ' 5870c6d8-6703-4b27-8ae4-687b4ca7caea ' em uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="1eb8e-116">Exemplo 3: usando a ID do recurso operação</span><span class="sxs-lookup"><span data-stu-id="1eb8e-116">Example 3: Using operation resource id</span></span>
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
```

<span data-ttu-id="1eb8e-117">Este comando obtém a operação com a ID '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea '.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="1eb8e-118">OS</span><span class="sxs-lookup"><span data-stu-id="1eb8e-118">PARAMETERS</span></span>

### <span data-ttu-id="1eb8e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb8e-119">-DefaultProfile</span></span>
<span data-ttu-id="1eb8e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb8e-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="1eb8e-121">-ManagedInstanceName</span></span>
<span data-ttu-id="1eb8e-122">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-122">The name of the instance.</span></span>

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

### <span data-ttu-id="1eb8e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="1eb8e-123">-Name</span></span>
<span data-ttu-id="1eb8e-124">O nome da operação.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-124">The name of the operation.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb8e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb8e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1eb8e-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="1eb8e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eb8e-127">-ResourceId</span></span>
<span data-ttu-id="1eb8e-128">O identificador de recursos da operação de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-128">The managed instance operation resource identifier.</span></span>

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

### <span data-ttu-id="1eb8e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb8e-129">CommonParameters</span></span>
<span data-ttu-id="1eb8e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb8e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb8e-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eb8e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb8e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1eb8e-132">INPUTS</span></span>

### <span data-ttu-id="1eb8e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb8e-133">System.String</span></span>

## <span data-ttu-id="1eb8e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1eb8e-134">OUTPUTS</span></span>

### <span data-ttu-id="1eb8e-135">Microsoft. Azure. Commands. Sql. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="1eb8e-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="1eb8e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1eb8e-136">NOTES</span></span>

## <span data-ttu-id="1eb8e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eb8e-137">RELATED LINKS</span></span>
