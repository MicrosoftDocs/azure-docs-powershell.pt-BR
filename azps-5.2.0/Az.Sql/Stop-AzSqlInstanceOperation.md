---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264135"
---
# <span data-ttu-id="d34b3-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="d34b3-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="d34b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d34b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d34b3-103">Interrompe as operações de uma instância gerenciada de SQL.</span><span class="sxs-lookup"><span data-stu-id="d34b3-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="d34b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d34b3-104">SYNTAX</span></span>

### <span data-ttu-id="d34b3-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d34b3-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d34b3-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d34b3-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d34b3-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d34b3-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d34b3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d34b3-108">DESCRIPTION</span></span>
<span data-ttu-id="d34b3-109">O cmdlet Stop-AzSqlInstanceOperation interrompe a operação com o nome de operação fornecido em uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="d34b3-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="d34b3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d34b3-110">EXAMPLES</span></span>

### <span data-ttu-id="d34b3-111">Exemplo 1: obter uma operação específica</span><span class="sxs-lookup"><span data-stu-id="d34b3-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="d34b3-112">Este comando interrompe a operação com o nome ' d0f5bef5-e2b1-4ef8-bb42-2e54073874f9 ' em uma instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="d34b3-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="d34b3-113">Exemplo 2: usando a ID do recurso operação</span><span class="sxs-lookup"><span data-stu-id="d34b3-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="d34b3-114">Este comando interrompe a operação com ID do recurso $managedInstanceOperation. ID.</span><span class="sxs-lookup"><span data-stu-id="d34b3-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="d34b3-115">Exemplo 3: usando o objeto Operation</span><span class="sxs-lookup"><span data-stu-id="d34b3-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="d34b3-116">Esse comando interrompe a operação com o objeto $managedInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="d34b3-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="d34b3-117">OS</span><span class="sxs-lookup"><span data-stu-id="d34b3-117">PARAMETERS</span></span>

### <span data-ttu-id="d34b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34b3-118">-DefaultProfile</span></span>
<span data-ttu-id="d34b3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d34b3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d34b3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d34b3-120">-Force</span></span>
<span data-ttu-id="d34b3-121">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="d34b3-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d34b3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d34b3-122">-InputObject</span></span>
<span data-ttu-id="d34b3-123">A operação a ser cancelada</span><span class="sxs-lookup"><span data-stu-id="d34b3-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d34b3-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="d34b3-124">-ManagedInstanceName</span></span>
<span data-ttu-id="d34b3-125">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="d34b3-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34b3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d34b3-126">-Name</span></span>
<span data-ttu-id="d34b3-127">O nome da operação.</span><span class="sxs-lookup"><span data-stu-id="d34b3-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34b3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34b3-128">-ResourceGroupName</span></span>
<span data-ttu-id="d34b3-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d34b3-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34b3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d34b3-130">-ResourceId</span></span>
<span data-ttu-id="d34b3-131">A ID do recurso do objeto de operação para parar</span><span class="sxs-lookup"><span data-stu-id="d34b3-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d34b3-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d34b3-132">-Confirm</span></span>
<span data-ttu-id="d34b3-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d34b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d34b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34b3-134">-WhatIf</span></span>
<span data-ttu-id="d34b3-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d34b3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d34b3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d34b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d34b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34b3-137">CommonParameters</span></span>
<span data-ttu-id="d34b3-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34b3-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d34b3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34b3-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d34b3-140">INPUTS</span></span>

### <span data-ttu-id="d34b3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d34b3-141">System.String</span></span>

### <span data-ttu-id="d34b3-142">Microsoft. Azure. Commands. Sql. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="d34b3-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="d34b3-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d34b3-143">OUTPUTS</span></span>

### <span data-ttu-id="d34b3-144">Microsoft. Azure. Commands. Sql. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="d34b3-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="d34b3-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d34b3-145">NOTES</span></span>

## <span data-ttu-id="d34b3-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d34b3-146">RELATED LINKS</span></span>
