---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115684"
---
# <span data-ttu-id="3e20b-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="3e20b-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="3e20b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e20b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e20b-103">Obter um ou mais Ouvintes de Grupo de Disponibilidade em um SQL Virtual Machine Group.</span><span class="sxs-lookup"><span data-stu-id="3e20b-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="3e20b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e20b-104">SYNTAX</span></span>

### <span data-ttu-id="3e20b-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3e20b-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e20b-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="3e20b-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e20b-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="3e20b-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e20b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e20b-108">DESCRIPTION</span></span>
<span data-ttu-id="3e20b-109">A Get-AzAvailabilityGroupListener obtém um ou mais Ouvintes do Grupo de Disponibilidade do SQL Virtual Machine Group.</span><span class="sxs-lookup"><span data-stu-id="3e20b-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="3e20b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e20b-110">EXAMPLES</span></span>

### <span data-ttu-id="3e20b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e20b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="3e20b-112">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="3e20b-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3e20b-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3e20b-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="3e20b-114">Esse comando obtém informações sobre o AgListener01 do Ouvinte do Grupo de Disponibilidade no SQL Virtual Machine Group SqlVmGroup01 e Resource Group ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3e20b-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="3e20b-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3e20b-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="3e20b-116">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="3e20b-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3e20b-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3e20b-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="3e20b-118">Esse comando obtém informações sobre todos os Ouvintes do Grupo de Disponibilidade no SQL Virtual Machine Group SqlVmGroup01 e Resource Group ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3e20b-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="3e20b-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3e20b-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="3e20b-120">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="3e20b-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3e20b-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3e20b-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="3e20b-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e20b-122">PARAMETERS</span></span>

### <span data-ttu-id="3e20b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e20b-123">-DefaultProfile</span></span>
<span data-ttu-id="3e20b-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e20b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e20b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e20b-125">-Name</span></span>
<span data-ttu-id="3e20b-126">Nome do Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="3e20b-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e20b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e20b-127">-ResourceGroupName</span></span>
<span data-ttu-id="3e20b-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e20b-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e20b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e20b-129">-ResourceId</span></span>
<span data-ttu-id="3e20b-130">ID do Recurso de Ouvinte do Grupo de Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="3e20b-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e20b-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="3e20b-131">-SqlVMGroupName</span></span>
<span data-ttu-id="3e20b-132">Nome do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="3e20b-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e20b-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="3e20b-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="3e20b-134">Objeto do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="3e20b-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e20b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e20b-135">CommonParameters</span></span>
<span data-ttu-id="3e20b-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e20b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e20b-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e20b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e20b-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e20b-138">INPUTS</span></span>

### <span data-ttu-id="3e20b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3e20b-139">System.String</span></span>

### <span data-ttu-id="3e20b-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="3e20b-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="3e20b-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e20b-141">OUTPUTS</span></span>

### <span data-ttu-id="3e20b-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="3e20b-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="3e20b-143">Notas</span><span class="sxs-lookup"><span data-stu-id="3e20b-143">NOTES</span></span>

## <span data-ttu-id="3e20b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e20b-144">RELATED LINKS</span></span>
