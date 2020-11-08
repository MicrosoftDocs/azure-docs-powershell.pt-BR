---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111285"
---
# <span data-ttu-id="8d61e-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="8d61e-101">New-AzSqlVM</span></span>

## <span data-ttu-id="8d61e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d61e-102">SYNOPSIS</span></span>
<span data-ttu-id="8d61e-103">Cria uma nova máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="8d61e-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="8d61e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d61e-104">SYNTAX</span></span>

### <span data-ttu-id="8d61e-105">NameParamaterList (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d61e-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d61e-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="8d61e-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d61e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d61e-107">DESCRIPTION</span></span>
<span data-ttu-id="8d61e-108">O cmdlet New-AzSqlVM cria uma máquina virtual do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8d61e-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="8d61e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d61e-109">EXAMPLES</span></span>

### <span data-ttu-id="8d61e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d61e-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="8d61e-111">Cria uma nova máquina virtual do Azure SQL com o nome VM na ResourceGroup01 do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8d61e-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="8d61e-112">OS</span><span class="sxs-lookup"><span data-stu-id="8d61e-112">PARAMETERS</span></span>

### <span data-ttu-id="8d61e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d61e-113">-AsJob</span></span>
<span data-ttu-id="8d61e-114">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="8d61e-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="8d61e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d61e-115">-DefaultProfile</span></span>
<span data-ttu-id="8d61e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d61e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d61e-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8d61e-117">-LicenseType</span></span>
<span data-ttu-id="8d61e-118">Tipo de licença da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8d61e-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="8d61e-119">-Local</span><span class="sxs-lookup"><span data-stu-id="8d61e-119">-Location</span></span>
<span data-ttu-id="8d61e-120">Local da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8d61e-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="8d61e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d61e-121">-Name</span></span>
<span data-ttu-id="8d61e-122">Nome da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8d61e-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="8d61e-123">-Oferta</span><span class="sxs-lookup"><span data-stu-id="8d61e-123">-Offer</span></span>
<span data-ttu-id="8d61e-124">Oferta da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8d61e-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="8d61e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d61e-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d61e-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d61e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d61e-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="8d61e-127">-Sku</span></span>
<span data-ttu-id="8d61e-128">Tipo de edição da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8d61e-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="8d61e-129">-Sqlmanagementtype</span><span class="sxs-lookup"><span data-stu-id="8d61e-129">-SqlManagementType</span></span>
<span data-ttu-id="8d61e-130">Tipo de gerenciamento da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8d61e-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="8d61e-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="8d61e-131">-SqlVM</span></span>
<span data-ttu-id="8d61e-132">Objeto da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8d61e-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="8d61e-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="8d61e-133">-Tag</span></span>
<span data-ttu-id="8d61e-134">As marcas a serem associadas à máquina virtual do SQL</span><span class="sxs-lookup"><span data-stu-id="8d61e-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="8d61e-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d61e-135">-Confirm</span></span>
<span data-ttu-id="8d61e-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d61e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d61e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d61e-137">-WhatIf</span></span>
<span data-ttu-id="8d61e-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d61e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d61e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d61e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d61e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d61e-140">CommonParameters</span></span>
<span data-ttu-id="8d61e-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d61e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d61e-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d61e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d61e-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d61e-143">INPUTS</span></span>

### <span data-ttu-id="8d61e-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="8d61e-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="8d61e-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d61e-145">OUTPUTS</span></span>

### <span data-ttu-id="8d61e-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="8d61e-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="8d61e-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d61e-147">NOTES</span></span>

## <span data-ttu-id="8d61e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d61e-148">RELATED LINKS</span></span>
