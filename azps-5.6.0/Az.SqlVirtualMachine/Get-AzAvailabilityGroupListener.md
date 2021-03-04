---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: be20b280dccccae6f6afcc1a18514ad3dfb89ba2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892694"
---
# <span data-ttu-id="dcadb-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="dcadb-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="dcadb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcadb-102">SYNOPSIS</span></span>
<span data-ttu-id="dcadb-103">Obter um ou mais Ouvintes de Grupo de Disponibilidade em um SQL Virtual Machine Group.</span><span class="sxs-lookup"><span data-stu-id="dcadb-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="dcadb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dcadb-104">SYNTAX</span></span>

### <span data-ttu-id="dcadb-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dcadb-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcadb-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="dcadb-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcadb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcadb-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcadb-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dcadb-108">DESCRIPTION</span></span>
<span data-ttu-id="dcadb-109">O Get-AzAvailabilityGroupListener obtém um ou mais Ouvintes de Grupo de Disponibilidade do SQL Virtual Machine Group.</span><span class="sxs-lookup"><span data-stu-id="dcadb-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="dcadb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcadb-110">EXAMPLES</span></span>

### <span data-ttu-id="dcadb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dcadb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="dcadb-112">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="dcadb-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="dcadb-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="dcadb-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="dcadb-114">Este comando obtém informações sobre o Ouvinte do Grupo de Disponibilidade AgListener01 no grupo de máquinas virtuais SQL SqlVmGroup01 e ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="dcadb-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="dcadb-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dcadb-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="dcadb-116">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="dcadb-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="dcadb-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="dcadb-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="dcadb-118">Este comando obtém informações sobre todos os Ouvintes do Grupo de Disponibilidade no grupo de máquinas virtuais SQL SqlVmGroup01 e ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="dcadb-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="dcadb-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dcadb-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="dcadb-120">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="dcadb-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="dcadb-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="dcadb-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="dcadb-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dcadb-122">PARAMETERS</span></span>

### <span data-ttu-id="dcadb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcadb-123">-DefaultProfile</span></span>
<span data-ttu-id="dcadb-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcadb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcadb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dcadb-125">-Name</span></span>
<span data-ttu-id="dcadb-126">Nome do Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="dcadb-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="dcadb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcadb-127">-ResourceGroupName</span></span>
<span data-ttu-id="dcadb-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dcadb-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="dcadb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcadb-129">-ResourceId</span></span>
<span data-ttu-id="dcadb-130">ID do Recurso ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="dcadb-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="dcadb-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="dcadb-131">-SqlVMGroupName</span></span>
<span data-ttu-id="dcadb-132">SQL nome do grupo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dcadb-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="dcadb-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="dcadb-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="dcadb-134">SQL objeto Group da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dcadb-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="dcadb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcadb-135">CommonParameters</span></span>
<span data-ttu-id="dcadb-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcadb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcadb-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcadb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcadb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcadb-138">INPUTS</span></span>

### <span data-ttu-id="dcadb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dcadb-139">System.String</span></span>

### <span data-ttu-id="dcadb-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="dcadb-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="dcadb-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dcadb-141">OUTPUTS</span></span>

### <span data-ttu-id="dcadb-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="dcadb-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="dcadb-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="dcadb-143">NOTES</span></span>

## <span data-ttu-id="dcadb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcadb-144">RELATED LINKS</span></span>
