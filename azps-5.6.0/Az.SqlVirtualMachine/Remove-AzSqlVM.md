---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 741db1ddd4d2cce236d5a1d6787ea25179aa373f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888636"
---
# <span data-ttu-id="8583b-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="8583b-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="8583b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8583b-102">SYNOPSIS</span></span>
<span data-ttu-id="8583b-103">Exclui uma máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="8583b-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="8583b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8583b-104">SYNTAX</span></span>

### <span data-ttu-id="8583b-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8583b-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8583b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8583b-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8583b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8583b-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8583b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8583b-108">DESCRIPTION</span></span>
<span data-ttu-id="8583b-109">O Remove-AzSqlVM cmdlet exclui uma máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="8583b-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="8583b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8583b-110">EXAMPLES</span></span>

### <span data-ttu-id="8583b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8583b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="8583b-112">Exclui o Azure SQL "vm" da máquina virtual no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8583b-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8583b-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8583b-113">PARAMETERS</span></span>

### <span data-ttu-id="8583b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8583b-114">-AsJob</span></span>
<span data-ttu-id="8583b-115">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="8583b-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="8583b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8583b-116">-DefaultProfile</span></span>
<span data-ttu-id="8583b-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8583b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8583b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8583b-118">-InputObject</span></span>
<span data-ttu-id="8583b-119">SQL objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8583b-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8583b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8583b-120">-Name</span></span>
<span data-ttu-id="8583b-121">SQL nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8583b-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8583b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8583b-122">-PassThru</span></span>
<span data-ttu-id="8583b-123">Especifica se o recurso excluído deve ser produzido no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8583b-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="8583b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8583b-124">-ResourceGroupName</span></span>
<span data-ttu-id="8583b-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8583b-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="8583b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8583b-126">-ResourceId</span></span>
<span data-ttu-id="8583b-127">SQL id de recurso de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8583b-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8583b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8583b-128">-Confirm</span></span>
<span data-ttu-id="8583b-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8583b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8583b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8583b-130">-WhatIf</span></span>
<span data-ttu-id="8583b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8583b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8583b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8583b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8583b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8583b-133">CommonParameters</span></span>
<span data-ttu-id="8583b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8583b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8583b-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8583b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8583b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8583b-136">INPUTS</span></span>

### <span data-ttu-id="8583b-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="8583b-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="8583b-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8583b-138">OUTPUTS</span></span>

### <span data-ttu-id="8583b-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="8583b-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="8583b-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="8583b-140">NOTES</span></span>

## <span data-ttu-id="8583b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8583b-141">RELATED LINKS</span></span>
