---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429639"
---
# <span data-ttu-id="2ceb3-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="2ceb3-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="2ceb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ceb3-102">SYNOPSIS</span></span>
<span data-ttu-id="2ceb3-103">Exclui um ouvinte de grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="2ceb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ceb3-104">SYNTAX</span></span>

### <span data-ttu-id="2ceb3-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ceb3-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ceb3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ceb3-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ceb3-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="2ceb3-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ceb3-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="2ceb3-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ceb3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ceb3-109">DESCRIPTION</span></span>
<span data-ttu-id="2ceb3-110">O cmdlet Remove-AzAvailabilityGroupListener exclui um ouvinte de grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="2ceb3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ceb3-111">EXAMPLES</span></span>

### <span data-ttu-id="2ceb3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ceb3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="2ceb3-113">Nome ResourceGroupName Nome_do_grupo AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="2ceb3-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="2ceb3-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="2ceb3-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="2ceb3-115">Exclui a disponibilidade do ouvinte do grupo de AgListener01 no grupo de disponibilidade AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="2ceb3-116">OS</span><span class="sxs-lookup"><span data-stu-id="2ceb3-116">PARAMETERS</span></span>

### <span data-ttu-id="2ceb3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ceb3-117">-AsJob</span></span>
<span data-ttu-id="2ceb3-118">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2ceb3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ceb3-119">-DefaultProfile</span></span>
<span data-ttu-id="2ceb3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ceb3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ceb3-121">-InputObject</span></span>
<span data-ttu-id="2ceb3-122">Objeto ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="2ceb3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ceb3-123">-Name</span></span>
<span data-ttu-id="2ceb3-124">Nome do ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="2ceb3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ceb3-125">-PassThru</span></span>
<span data-ttu-id="2ceb3-126">Especifica se o recurso excluído deve ser impresso no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="2ceb3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ceb3-127">-ResourceGroupName</span></span>
<span data-ttu-id="2ceb3-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="2ceb3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ceb3-129">-ResourceId</span></span>
<span data-ttu-id="2ceb3-130">ID do recurso do ouvinte de grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="2ceb3-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="2ceb3-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="2ceb3-131">-SqlVMGroupName</span></span>
<span data-ttu-id="2ceb3-132">Nome do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="2ceb3-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="2ceb3-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="2ceb3-134">Objeto de grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="2ceb3-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2ceb3-135">-Confirm</span></span>
<span data-ttu-id="2ceb3-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ceb3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ceb3-137">-WhatIf</span></span>
<span data-ttu-id="2ceb3-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ceb3-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ceb3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ceb3-140">CommonParameters</span></span>
<span data-ttu-id="2ceb3-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ceb3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ceb3-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ceb3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ceb3-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ceb3-143">INPUTS</span></span>

### <span data-ttu-id="2ceb3-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="2ceb3-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="2ceb3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2ceb3-145">System.String</span></span>

### <span data-ttu-id="2ceb3-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="2ceb3-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="2ceb3-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ceb3-147">OUTPUTS</span></span>

### <span data-ttu-id="2ceb3-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="2ceb3-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="2ceb3-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ceb3-149">NOTES</span></span>

## <span data-ttu-id="2ceb3-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ceb3-150">RELATED LINKS</span></span>
