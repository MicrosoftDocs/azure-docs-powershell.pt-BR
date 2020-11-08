---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115643"
---
# <span data-ttu-id="55a11-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="55a11-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="55a11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55a11-102">SYNOPSIS</span></span>
<span data-ttu-id="55a11-103">Exclui uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="55a11-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="55a11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55a11-104">SYNTAX</span></span>

### <span data-ttu-id="55a11-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="55a11-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a11-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="55a11-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55a11-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="55a11-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a11-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55a11-108">DESCRIPTION</span></span>
<span data-ttu-id="55a11-109">O cmdlet Remove-AzSqlVM exclui uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="55a11-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="55a11-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55a11-110">EXAMPLES</span></span>

### <span data-ttu-id="55a11-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55a11-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="55a11-112">Exclui a "VM" da máquina virtual do Azure SQL no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="55a11-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="55a11-113">OS</span><span class="sxs-lookup"><span data-stu-id="55a11-113">PARAMETERS</span></span>

### <span data-ttu-id="55a11-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55a11-114">-AsJob</span></span>
<span data-ttu-id="55a11-115">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="55a11-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="55a11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a11-116">-DefaultProfile</span></span>
<span data-ttu-id="55a11-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55a11-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a11-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55a11-118">-InputObject</span></span>
<span data-ttu-id="55a11-119">Objeto da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="55a11-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="55a11-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="55a11-120">-Name</span></span>
<span data-ttu-id="55a11-121">Nome da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="55a11-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="55a11-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55a11-122">-PassThru</span></span>
<span data-ttu-id="55a11-123">Especifica se o recurso excluído deve ser impresso no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55a11-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="55a11-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a11-124">-ResourceGroupName</span></span>
<span data-ttu-id="55a11-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="55a11-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="55a11-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55a11-126">-ResourceId</span></span>
<span data-ttu-id="55a11-127">ID do recurso da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="55a11-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="55a11-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55a11-128">-Confirm</span></span>
<span data-ttu-id="55a11-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55a11-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a11-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a11-130">-WhatIf</span></span>
<span data-ttu-id="55a11-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55a11-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a11-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55a11-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a11-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a11-133">CommonParameters</span></span>
<span data-ttu-id="55a11-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a11-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a11-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55a11-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a11-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55a11-136">INPUTS</span></span>

### <span data-ttu-id="55a11-137">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="55a11-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="55a11-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55a11-138">OUTPUTS</span></span>

### <span data-ttu-id="55a11-139">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="55a11-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="55a11-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55a11-140">NOTES</span></span>

## <span data-ttu-id="55a11-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55a11-141">RELATED LINKS</span></span>
