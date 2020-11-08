---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110800"
---
# <span data-ttu-id="d81f4-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="d81f4-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="d81f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d81f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d81f4-103">Exclui uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="d81f4-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="d81f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d81f4-104">SYNTAX</span></span>

### <span data-ttu-id="d81f4-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="d81f4-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d81f4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d81f4-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d81f4-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="d81f4-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d81f4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d81f4-108">DESCRIPTION</span></span>
<span data-ttu-id="d81f4-109">O cmdlet Remove-AzSqlVM exclui uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="d81f4-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="d81f4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d81f4-110">EXAMPLES</span></span>

### <span data-ttu-id="d81f4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d81f4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="d81f4-112">Exclui a "VM" da máquina virtual do Azure SQL no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d81f4-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="d81f4-113">OS</span><span class="sxs-lookup"><span data-stu-id="d81f4-113">PARAMETERS</span></span>

### <span data-ttu-id="d81f4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d81f4-114">-AsJob</span></span>
<span data-ttu-id="d81f4-115">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d81f4-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d81f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81f4-116">-DefaultProfile</span></span>
<span data-ttu-id="d81f4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d81f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d81f4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d81f4-118">-InputObject</span></span>
<span data-ttu-id="d81f4-119">Objeto da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="d81f4-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="d81f4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d81f4-120">-Name</span></span>
<span data-ttu-id="d81f4-121">Nome da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="d81f4-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="d81f4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d81f4-122">-PassThru</span></span>
<span data-ttu-id="d81f4-123">Especifica se o recurso excluído deve ser impresso no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d81f4-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="d81f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="d81f4-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d81f4-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d81f4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d81f4-126">-ResourceId</span></span>
<span data-ttu-id="d81f4-127">ID do recurso da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="d81f4-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="d81f4-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d81f4-128">-Confirm</span></span>
<span data-ttu-id="d81f4-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d81f4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d81f4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d81f4-130">-WhatIf</span></span>
<span data-ttu-id="d81f4-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d81f4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d81f4-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d81f4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d81f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81f4-133">CommonParameters</span></span>
<span data-ttu-id="d81f4-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d81f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81f4-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d81f4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81f4-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d81f4-136">INPUTS</span></span>

### <span data-ttu-id="d81f4-137">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d81f4-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d81f4-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d81f4-138">OUTPUTS</span></span>

### <span data-ttu-id="d81f4-139">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d81f4-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d81f4-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d81f4-140">NOTES</span></span>

## <span data-ttu-id="d81f4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d81f4-141">RELATED LINKS</span></span>
