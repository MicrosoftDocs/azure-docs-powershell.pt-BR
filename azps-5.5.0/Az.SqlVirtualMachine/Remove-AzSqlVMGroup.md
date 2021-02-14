---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111288"
---
# <span data-ttu-id="f0974-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="f0974-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="f0974-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0974-102">SYNOPSIS</span></span>
<span data-ttu-id="f0974-103">Exclui um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="f0974-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="f0974-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0974-104">SYNTAX</span></span>

### <span data-ttu-id="f0974-105">Lista de Paramater (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f0974-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0974-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f0974-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0974-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="f0974-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0974-108">Nome</span><span class="sxs-lookup"><span data-stu-id="f0974-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0974-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0974-109">DESCRIPTION</span></span>
<span data-ttu-id="f0974-110">O Remove-AzSqlVMGroup cmdlet exclui um grupo de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="f0974-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="f0974-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0974-111">EXAMPLES</span></span>

### <span data-ttu-id="f0974-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0974-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="f0974-113">Exclui o grupo de máquina virtual SQL do Azure "grupo de teste" no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f0974-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f0974-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0974-114">PARAMETERS</span></span>

### <span data-ttu-id="f0974-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0974-115">-AsJob</span></span>
<span data-ttu-id="f0974-116">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f0974-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f0974-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0974-117">-DefaultProfile</span></span>
<span data-ttu-id="f0974-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0974-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0974-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0974-119">-InputObject</span></span>
<span data-ttu-id="f0974-120">Objeto de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="f0974-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="f0974-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0974-121">-Name</span></span>
<span data-ttu-id="f0974-122">Nome do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="f0974-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="f0974-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0974-123">-PassThru</span></span>
<span data-ttu-id="f0974-124">Especifica se o recurso excluído será saída no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0974-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="f0974-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0974-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0974-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0974-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0974-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0974-127">-ResourceId</span></span>
<span data-ttu-id="f0974-128">ID do recurso do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="f0974-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="f0974-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f0974-129">-Confirm</span></span>
<span data-ttu-id="f0974-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0974-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0974-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0974-131">-WhatIf</span></span>
<span data-ttu-id="f0974-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f0974-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0974-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0974-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0974-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0974-134">CommonParameters</span></span>
<span data-ttu-id="f0974-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0974-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0974-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0974-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0974-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="f0974-137">INPUTS</span></span>

### <span data-ttu-id="f0974-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="f0974-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="f0974-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f0974-139">System.String</span></span>

## <span data-ttu-id="f0974-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="f0974-140">OUTPUTS</span></span>

### <span data-ttu-id="f0974-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="f0974-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="f0974-142">Notas</span><span class="sxs-lookup"><span data-stu-id="f0974-142">NOTES</span></span>

## <span data-ttu-id="f0974-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0974-143">RELATED LINKS</span></span>
