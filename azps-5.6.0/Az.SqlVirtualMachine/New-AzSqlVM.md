---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: f7afae369258a30a156ff0439407fb4e4e4ef732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892691"
---
# <span data-ttu-id="fa55a-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="fa55a-101">New-AzSqlVM</span></span>

## <span data-ttu-id="fa55a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa55a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa55a-103">Cria uma nova máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="fa55a-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="fa55a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fa55a-104">SYNTAX</span></span>

### <span data-ttu-id="fa55a-105">NameParamaterList (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fa55a-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa55a-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="fa55a-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa55a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fa55a-107">DESCRIPTION</span></span>
<span data-ttu-id="fa55a-108">O New-AzSqlVM cmdlet cria uma máquina virtual do Azure SQL virtual.</span><span class="sxs-lookup"><span data-stu-id="fa55a-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="fa55a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa55a-109">EXAMPLES</span></span>

### <span data-ttu-id="fa55a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa55a-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="fa55a-111">Cria uma nova máquina SQL virtual do Azure com nome vm no grupo de recursos ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="fa55a-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="fa55a-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fa55a-112">PARAMETERS</span></span>

### <span data-ttu-id="fa55a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa55a-113">-AsJob</span></span>
<span data-ttu-id="fa55a-114">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fa55a-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fa55a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa55a-115">-DefaultProfile</span></span>
<span data-ttu-id="fa55a-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa55a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa55a-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fa55a-117">-LicenseType</span></span>
<span data-ttu-id="fa55a-118">SQL tipo de licença de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa55a-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa55a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="fa55a-119">-Location</span></span>
<span data-ttu-id="fa55a-120">SQL local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa55a-120">SQL virtual machine location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa55a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fa55a-121">-Name</span></span>
<span data-ttu-id="fa55a-122">SQL nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa55a-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa55a-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="fa55a-123">-Offer</span></span>
<span data-ttu-id="fa55a-124">SQL de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa55a-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa55a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa55a-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa55a-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa55a-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa55a-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="fa55a-127">-Sku</span></span>
<span data-ttu-id="fa55a-128">SQL tipo de edição de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa55a-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa55a-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="fa55a-129">-SqlManagementType</span></span>
<span data-ttu-id="fa55a-130">SQL tipo de gerenciamento de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa55a-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa55a-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="fa55a-131">-SqlVM</span></span>
<span data-ttu-id="fa55a-132">SQL objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa55a-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa55a-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="fa55a-133">-Tag</span></span>
<span data-ttu-id="fa55a-134">As marcas a associar à máquina SQL virtual</span><span class="sxs-lookup"><span data-stu-id="fa55a-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa55a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa55a-135">-Confirm</span></span>
<span data-ttu-id="fa55a-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa55a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa55a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa55a-137">-WhatIf</span></span>
<span data-ttu-id="fa55a-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa55a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa55a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa55a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa55a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa55a-140">CommonParameters</span></span>
<span data-ttu-id="fa55a-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa55a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa55a-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa55a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa55a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa55a-143">INPUTS</span></span>

### <span data-ttu-id="fa55a-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="fa55a-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="fa55a-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fa55a-145">OUTPUTS</span></span>

### <span data-ttu-id="fa55a-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="fa55a-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="fa55a-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="fa55a-147">NOTES</span></span>

## <span data-ttu-id="fa55a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa55a-148">RELATED LINKS</span></span>
