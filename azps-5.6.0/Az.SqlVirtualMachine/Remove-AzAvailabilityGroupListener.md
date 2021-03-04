---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: 56891d1dae20f89289b9c2f72bf87bfeed7bd347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888642"
---
# <span data-ttu-id="0442c-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="0442c-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="0442c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0442c-102">SYNOPSIS</span></span>
<span data-ttu-id="0442c-103">Exclui um Ouvinte de Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="0442c-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="0442c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0442c-104">SYNTAX</span></span>

### <span data-ttu-id="0442c-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0442c-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0442c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0442c-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0442c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0442c-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0442c-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="0442c-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0442c-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0442c-109">DESCRIPTION</span></span>
<span data-ttu-id="0442c-110">O cmdlet Remove-AzAvailabilityGroupListener exclui um Ouvinte de Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="0442c-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="0442c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0442c-111">EXAMPLES</span></span>

### <span data-ttu-id="0442c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0442c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="0442c-113">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="0442c-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="0442c-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="0442c-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="0442c-115">Exclui o Ouvinte do Grupo de Disponibilidade AgListener01 no Grupo de Disponibilidade AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="0442c-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="0442c-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0442c-116">PARAMETERS</span></span>

### <span data-ttu-id="0442c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0442c-117">-AsJob</span></span>
<span data-ttu-id="0442c-118">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0442c-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0442c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0442c-119">-DefaultProfile</span></span>
<span data-ttu-id="0442c-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0442c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0442c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0442c-121">-InputObject</span></span>
<span data-ttu-id="0442c-122">Objeto Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="0442c-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0442c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0442c-123">-Name</span></span>
<span data-ttu-id="0442c-124">Nome do Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="0442c-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0442c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0442c-125">-PassThru</span></span>
<span data-ttu-id="0442c-126">Especifica se o recurso excluído deve ser produzido no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0442c-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="0442c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0442c-127">-ResourceGroupName</span></span>
<span data-ttu-id="0442c-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0442c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="0442c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0442c-129">-ResourceId</span></span>
<span data-ttu-id="0442c-130">ID do Recurso ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="0442c-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="0442c-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="0442c-131">-SqlVMGroupName</span></span>
<span data-ttu-id="0442c-132">SQL nome do grupo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0442c-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="0442c-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="0442c-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="0442c-134">SQL objeto Group da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0442c-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="0442c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0442c-135">-Confirm</span></span>
<span data-ttu-id="0442c-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0442c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0442c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0442c-137">-WhatIf</span></span>
<span data-ttu-id="0442c-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0442c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0442c-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0442c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0442c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0442c-140">CommonParameters</span></span>
<span data-ttu-id="0442c-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0442c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0442c-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0442c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0442c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0442c-143">INPUTS</span></span>

### <span data-ttu-id="0442c-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="0442c-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="0442c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0442c-145">System.String</span></span>

### <span data-ttu-id="0442c-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="0442c-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="0442c-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0442c-147">OUTPUTS</span></span>

### <span data-ttu-id="0442c-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="0442c-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="0442c-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="0442c-149">NOTES</span></span>

## <span data-ttu-id="0442c-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0442c-150">RELATED LINKS</span></span>
