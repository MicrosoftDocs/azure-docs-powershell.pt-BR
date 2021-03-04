---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: a7ff8df963f7d1d58256ab40cf5788e81b49a23c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890550"
---
# <span data-ttu-id="73559-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="73559-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="73559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73559-102">SYNOPSIS</span></span>
<span data-ttu-id="73559-103">Obtém um ou mais grupos de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="73559-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="73559-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="73559-104">SYNTAX</span></span>

### <span data-ttu-id="73559-105">ResourceGroupOnly (Padrão)</span><span class="sxs-lookup"><span data-stu-id="73559-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73559-106">Nome</span><span class="sxs-lookup"><span data-stu-id="73559-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73559-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="73559-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73559-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="73559-108">DESCRIPTION</span></span>
<span data-ttu-id="73559-109">O Get-AzSqlVMGroup cmdlet obtém um ou mais grupos de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="73559-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="73559-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73559-110">EXAMPLES</span></span>

### <span data-ttu-id="73559-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73559-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="73559-112">Este comando obtém informações sobre todos os grupos de máquinas virtuais do Azure SQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="73559-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="73559-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="73559-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="73559-114">Este comando obtém informações sobre todos os grupos de máquinas virtuais do Azure SQL na assinatura atual atribuída ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="73559-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="73559-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="73559-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="73559-116">Este comando obtém informações sobre SQL grupo de máquinas virtuais "test-group" atribuído ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="73559-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="73559-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="73559-117">PARAMETERS</span></span>

### <span data-ttu-id="73559-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73559-118">-DefaultProfile</span></span>
<span data-ttu-id="73559-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73559-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73559-120">-Name</span><span class="sxs-lookup"><span data-stu-id="73559-120">-Name</span></span>
<span data-ttu-id="73559-121">SQL nome do grupo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="73559-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="73559-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73559-122">-ResourceGroupName</span></span>
<span data-ttu-id="73559-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73559-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="73559-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73559-124">-ResourceId</span></span>
<span data-ttu-id="73559-125">SQL id de recurso do grupo de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="73559-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="73559-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73559-126">CommonParameters</span></span>
<span data-ttu-id="73559-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73559-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73559-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73559-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73559-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73559-129">INPUTS</span></span>

### <span data-ttu-id="73559-130">System.String</span><span class="sxs-lookup"><span data-stu-id="73559-130">System.String</span></span>

## <span data-ttu-id="73559-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="73559-131">OUTPUTS</span></span>

### <span data-ttu-id="73559-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="73559-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="73559-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="73559-133">NOTES</span></span>

## <span data-ttu-id="73559-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73559-134">RELATED LINKS</span></span>
