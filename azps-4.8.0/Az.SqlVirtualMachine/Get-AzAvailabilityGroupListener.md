---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113221"
---
# <span data-ttu-id="98869-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="98869-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="98869-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98869-102">SYNOPSIS</span></span>
<span data-ttu-id="98869-103">Obter um ou mais ouvintes do grupo de disponibilidade em um grupo de máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="98869-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="98869-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98869-104">SYNTAX</span></span>

### <span data-ttu-id="98869-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="98869-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98869-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="98869-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98869-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="98869-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98869-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98869-108">DESCRIPTION</span></span>
<span data-ttu-id="98869-109">O Get-AzAvailabilityGroupListener Obtém um ou mais Listeners do grupo de disponibilidade do grupo de máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="98869-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="98869-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98869-110">EXAMPLES</span></span>

### <span data-ttu-id="98869-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98869-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="98869-112">Nome ResourceGroupName Nome_do_grupo AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="98869-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="98869-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="98869-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="98869-114">Esse comando obtém informações sobre a AgListener01 do ouvinte do grupo de disponibilidade no SqlVmGroup01 de grupo da máquina virtual do SQL e ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="98869-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="98869-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="98869-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="98869-116">Nome ResourceGroupName Nome_do_grupo AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="98869-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="98869-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="98869-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="98869-118">Esse comando obtém informações sobre todos os ouvintes do grupo de disponibilidade no grupo de SqlVmGroup01 de máquina virtual SQL e ResourceGroup01 de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="98869-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="98869-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="98869-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="98869-120">Nome ResourceGroupName Nome_do_grupo AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="98869-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="98869-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="98869-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="98869-122">OS</span><span class="sxs-lookup"><span data-stu-id="98869-122">PARAMETERS</span></span>

### <span data-ttu-id="98869-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98869-123">-DefaultProfile</span></span>
<span data-ttu-id="98869-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98869-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98869-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="98869-125">-Name</span></span>
<span data-ttu-id="98869-126">Nome do ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="98869-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="98869-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98869-127">-ResourceGroupName</span></span>
<span data-ttu-id="98869-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="98869-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="98869-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98869-129">-ResourceId</span></span>
<span data-ttu-id="98869-130">ID do recurso do ouvinte de grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="98869-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="98869-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="98869-131">-SqlVMGroupName</span></span>
<span data-ttu-id="98869-132">Nome do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="98869-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="98869-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="98869-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="98869-134">Objeto de grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="98869-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="98869-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98869-135">CommonParameters</span></span>
<span data-ttu-id="98869-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98869-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98869-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98869-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98869-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98869-138">INPUTS</span></span>

### <span data-ttu-id="98869-139">System. String</span><span class="sxs-lookup"><span data-stu-id="98869-139">System.String</span></span>

### <span data-ttu-id="98869-140">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="98869-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="98869-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98869-141">OUTPUTS</span></span>

### <span data-ttu-id="98869-142">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="98869-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="98869-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98869-143">NOTES</span></span>

## <span data-ttu-id="98869-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98869-144">RELATED LINKS</span></span>
