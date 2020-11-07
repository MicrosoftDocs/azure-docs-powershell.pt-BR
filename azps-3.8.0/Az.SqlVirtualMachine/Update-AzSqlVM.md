---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: ce700b90194e1cd0fcdf05162696ae980d24ad01
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944187"
---
# <span data-ttu-id="8e489-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="8e489-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="8e489-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e489-102">SYNOPSIS</span></span>
<span data-ttu-id="8e489-103">Atualiza uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="8e489-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e489-104">SYNTAX</span></span>

### <span data-ttu-id="8e489-105">NameParamaterList (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e489-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e489-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="8e489-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e489-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="8e489-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e489-108">ResourceIdInputObject</span><span class="sxs-lookup"><span data-stu-id="8e489-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e489-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e489-109">DESCRIPTION</span></span>
<span data-ttu-id="8e489-110">O cmdlet Update-AzSqlVM atualiza uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="8e489-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e489-111">EXAMPLES</span></span>

### <span data-ttu-id="8e489-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e489-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="8e489-113">Atualiza as marcas de uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="8e489-114">OS</span><span class="sxs-lookup"><span data-stu-id="8e489-114">PARAMETERS</span></span>

### <span data-ttu-id="8e489-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e489-115">-AsJob</span></span>
<span data-ttu-id="8e489-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="8e489-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="8e489-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e489-117">-DefaultProfile</span></span>
<span data-ttu-id="8e489-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e489-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e489-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e489-119">-InputObject</span></span>
<span data-ttu-id="8e489-120">Objeto da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e489-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8e489-121">-LicenseType</span></span>
<span data-ttu-id="8e489-122">Tipo de licença da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e489-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e489-123">-Name</span></span>
<span data-ttu-id="8e489-124">Nome da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e489-125">-Oferta</span><span class="sxs-lookup"><span data-stu-id="8e489-125">-Offer</span></span>
<span data-ttu-id="8e489-126">Oferta da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e489-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e489-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e489-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e489-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e489-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e489-129">-ResourceId</span></span>
<span data-ttu-id="8e489-130">ID do recurso da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e489-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="8e489-131">-Sku</span></span>
<span data-ttu-id="8e489-132">Tipo de edição da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e489-133">-Sqlmanagementtype</span><span class="sxs-lookup"><span data-stu-id="8e489-133">-SqlManagementType</span></span>
<span data-ttu-id="8e489-134">Tipo de gerenciamento da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="8e489-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e489-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="8e489-135">-Tag</span></span>
<span data-ttu-id="8e489-136">As marcas a serem associadas à máquina virtual do SQL</span><span class="sxs-lookup"><span data-stu-id="8e489-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e489-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8e489-137">-Confirm</span></span>
<span data-ttu-id="8e489-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e489-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e489-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e489-139">-WhatIf</span></span>
<span data-ttu-id="8e489-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e489-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e489-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e489-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e489-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e489-142">CommonParameters</span></span>
<span data-ttu-id="8e489-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e489-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e489-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e489-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e489-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e489-145">INPUTS</span></span>

### <span data-ttu-id="8e489-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="8e489-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="8e489-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e489-147">OUTPUTS</span></span>

### <span data-ttu-id="8e489-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="8e489-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="8e489-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e489-149">NOTES</span></span>

## <span data-ttu-id="8e489-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e489-150">RELATED LINKS</span></span>
