---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: d9d5ee7159f5a7f237bd9194051c99801481f1d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888635"
---
# <span data-ttu-id="717cd-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="717cd-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="717cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="717cd-102">SYNOPSIS</span></span>
<span data-ttu-id="717cd-103">Exclui um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="717cd-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="717cd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="717cd-104">SYNTAX</span></span>

### <span data-ttu-id="717cd-105">ParamaterList (Padrão)</span><span class="sxs-lookup"><span data-stu-id="717cd-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="717cd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="717cd-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="717cd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="717cd-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="717cd-108">Nome</span><span class="sxs-lookup"><span data-stu-id="717cd-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="717cd-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="717cd-109">DESCRIPTION</span></span>
<span data-ttu-id="717cd-110">O Remove-AzSqlVMGroup cmdlet exclui um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="717cd-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="717cd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="717cd-111">EXAMPLES</span></span>

### <span data-ttu-id="717cd-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="717cd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="717cd-113">Exclui o grupo de SQL de máquinas virtuais do Azure "test-group" no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="717cd-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="717cd-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="717cd-114">PARAMETERS</span></span>

### <span data-ttu-id="717cd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="717cd-115">-AsJob</span></span>
<span data-ttu-id="717cd-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="717cd-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="717cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="717cd-117">-DefaultProfile</span></span>
<span data-ttu-id="717cd-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="717cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="717cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="717cd-119">-InputObject</span></span>
<span data-ttu-id="717cd-120">SQL objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="717cd-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="717cd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="717cd-121">-Name</span></span>
<span data-ttu-id="717cd-122">SQL nome do grupo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="717cd-122">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717cd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="717cd-123">-PassThru</span></span>
<span data-ttu-id="717cd-124">Especifica se o recurso excluído deve ser produzido no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="717cd-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="717cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="717cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="717cd-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="717cd-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="717cd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="717cd-127">-ResourceId</span></span>
<span data-ttu-id="717cd-128">SQL id de recurso do grupo de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="717cd-128">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="717cd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="717cd-129">-Confirm</span></span>
<span data-ttu-id="717cd-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="717cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="717cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="717cd-131">-WhatIf</span></span>
<span data-ttu-id="717cd-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="717cd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="717cd-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="717cd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="717cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717cd-134">CommonParameters</span></span>
<span data-ttu-id="717cd-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="717cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717cd-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="717cd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717cd-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="717cd-137">INPUTS</span></span>

### <span data-ttu-id="717cd-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="717cd-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="717cd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="717cd-139">System.String</span></span>

## <span data-ttu-id="717cd-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="717cd-140">OUTPUTS</span></span>

### <span data-ttu-id="717cd-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="717cd-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="717cd-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="717cd-142">NOTES</span></span>

## <span data-ttu-id="717cd-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="717cd-143">RELATED LINKS</span></span>
