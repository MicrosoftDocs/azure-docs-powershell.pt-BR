---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: 7af4302a17d15ba539a726ce84ef47bb1d574609
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773963"
---
# <span data-ttu-id="d1c8f-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="d1c8f-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="d1c8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c8f-103">Exclui um grupo da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="d1c8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1c8f-104">SYNTAX</span></span>

### <span data-ttu-id="d1c8f-105">ParamaterList (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1c8f-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1c8f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d1c8f-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1c8f-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="d1c8f-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1c8f-108">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="d1c8f-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1c8f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1c8f-109">DESCRIPTION</span></span>
<span data-ttu-id="d1c8f-110">O cmdlet Remove-AzSqlVMGroup exclui um grupo da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="d1c8f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1c8f-111">EXAMPLES</span></span>

### <span data-ttu-id="d1c8f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1c8f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="d1c8f-113">Exclui o "grupo de teste" do grupo de máquinas virtuais do Azure SQL na ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="d1c8f-114">OS</span><span class="sxs-lookup"><span data-stu-id="d1c8f-114">PARAMETERS</span></span>

### <span data-ttu-id="d1c8f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1c8f-115">-AsJob</span></span>
<span data-ttu-id="d1c8f-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d1c8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c8f-117">-DefaultProfile</span></span>
<span data-ttu-id="d1c8f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1c8f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1c8f-119">-InputObject</span></span>
<span data-ttu-id="d1c8f-120">Objeto da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="d1c8f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1c8f-121">-Name</span></span>
<span data-ttu-id="d1c8f-122">Nome do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="d1c8f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1c8f-123">-PassThru</span></span>
<span data-ttu-id="d1c8f-124">Especifica se o recurso excluído deve ser impresso no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="d1c8f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c8f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1c8f-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1c8f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1c8f-127">-ResourceId</span></span>
<span data-ttu-id="d1c8f-128">ID do recurso de grupo da máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="d1c8f-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d1c8f-129">-Confirm</span></span>
<span data-ttu-id="d1c8f-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1c8f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1c8f-131">-WhatIf</span></span>
<span data-ttu-id="d1c8f-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1c8f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1c8f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c8f-134">CommonParameters</span></span>
<span data-ttu-id="d1c8f-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c8f-136">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1c8f-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c8f-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1c8f-137">INPUTS</span></span>

### <span data-ttu-id="d1c8f-138">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="d1c8f-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="d1c8f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d1c8f-139">System.String</span></span>

## <span data-ttu-id="d1c8f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1c8f-140">OUTPUTS</span></span>

### <span data-ttu-id="d1c8f-141">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="d1c8f-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="d1c8f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1c8f-142">NOTES</span></span>

## <span data-ttu-id="d1c8f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1c8f-143">RELATED LINKS</span></span>
