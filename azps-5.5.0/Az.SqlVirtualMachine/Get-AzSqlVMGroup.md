---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112530"
---
# <span data-ttu-id="89711-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="89711-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="89711-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89711-102">SYNOPSIS</span></span>
<span data-ttu-id="89711-103">Recebe um ou mais grupos de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="89711-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="89711-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89711-104">SYNTAX</span></span>

### <span data-ttu-id="89711-105">ResourceGroupOnly (Padrão)</span><span class="sxs-lookup"><span data-stu-id="89711-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89711-106">Nome</span><span class="sxs-lookup"><span data-stu-id="89711-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89711-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="89711-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89711-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="89711-108">DESCRIPTION</span></span>
<span data-ttu-id="89711-109">O Get-AzSqlVMGroup cmdlet obtém um ou mais grupos de máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="89711-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="89711-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89711-110">EXAMPLES</span></span>

### <span data-ttu-id="89711-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89711-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="89711-112">Esse comando obtém informações sobre todos os grupos de máquinas virtuais SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="89711-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="89711-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="89711-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="89711-114">Esse comando obtém informações sobre todos os grupos de máquinas virtuais SQL do Azure na assinatura atual atribuída ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="89711-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="89711-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="89711-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="89711-116">Esse comando obtém informações sobre o grupo de máquina virtual SQL "grupo de teste" atribuído ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="89711-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="89711-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89711-117">PARAMETERS</span></span>

### <span data-ttu-id="89711-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89711-118">-DefaultProfile</span></span>
<span data-ttu-id="89711-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89711-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89711-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="89711-120">-Name</span></span>
<span data-ttu-id="89711-121">Nome do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="89711-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="89711-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89711-122">-ResourceGroupName</span></span>
<span data-ttu-id="89711-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="89711-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="89711-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89711-124">-ResourceId</span></span>
<span data-ttu-id="89711-125">ID do recurso do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="89711-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="89711-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89711-126">CommonParameters</span></span>
<span data-ttu-id="89711-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89711-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89711-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89711-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89711-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="89711-129">INPUTS</span></span>

### <span data-ttu-id="89711-130">System.String</span><span class="sxs-lookup"><span data-stu-id="89711-130">System.String</span></span>

## <span data-ttu-id="89711-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="89711-131">OUTPUTS</span></span>

### <span data-ttu-id="89711-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="89711-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="89711-133">Notas</span><span class="sxs-lookup"><span data-stu-id="89711-133">NOTES</span></span>

## <span data-ttu-id="89711-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89711-134">RELATED LINKS</span></span>
