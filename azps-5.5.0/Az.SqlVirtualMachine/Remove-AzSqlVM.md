---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113700"
---
# <span data-ttu-id="4db1c-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="4db1c-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="4db1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4db1c-102">SYNOPSIS</span></span>
<span data-ttu-id="4db1c-103">Exclui uma máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="4db1c-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="4db1c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4db1c-104">SYNTAX</span></span>

### <span data-ttu-id="4db1c-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4db1c-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db1c-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="4db1c-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db1c-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="4db1c-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4db1c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4db1c-108">DESCRIPTION</span></span>
<span data-ttu-id="4db1c-109">O Remove-AzSqlVM cmdlet exclui uma máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="4db1c-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="4db1c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4db1c-110">EXAMPLES</span></span>

### <span data-ttu-id="4db1c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4db1c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="4db1c-112">Exclui o "vm" da máquina virtual SQL do Azure no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4db1c-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="4db1c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4db1c-113">PARAMETERS</span></span>

### <span data-ttu-id="4db1c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4db1c-114">-AsJob</span></span>
<span data-ttu-id="4db1c-115">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4db1c-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4db1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db1c-116">-DefaultProfile</span></span>
<span data-ttu-id="4db1c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4db1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4db1c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4db1c-118">-InputObject</span></span>
<span data-ttu-id="4db1c-119">Objeto de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="4db1c-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="4db1c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4db1c-120">-Name</span></span>
<span data-ttu-id="4db1c-121">Nome da máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="4db1c-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="4db1c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4db1c-122">-PassThru</span></span>
<span data-ttu-id="4db1c-123">Especifica se o recurso excluído será saída no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4db1c-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="4db1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4db1c-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4db1c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="4db1c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4db1c-126">-ResourceId</span></span>
<span data-ttu-id="4db1c-127">ID do recurso de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="4db1c-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="4db1c-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4db1c-128">-Confirm</span></span>
<span data-ttu-id="4db1c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4db1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db1c-130">-WhatIf</span></span>
<span data-ttu-id="4db1c-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4db1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db1c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4db1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db1c-133">CommonParameters</span></span>
<span data-ttu-id="4db1c-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db1c-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4db1c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db1c-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="4db1c-136">INPUTS</span></span>

### <span data-ttu-id="4db1c-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="4db1c-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="4db1c-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="4db1c-138">OUTPUTS</span></span>

### <span data-ttu-id="4db1c-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="4db1c-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="4db1c-140">Notas</span><span class="sxs-lookup"><span data-stu-id="4db1c-140">NOTES</span></span>

## <span data-ttu-id="4db1c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4db1c-141">RELATED LINKS</span></span>
