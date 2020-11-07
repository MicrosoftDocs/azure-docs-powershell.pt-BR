---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777931"
---
# <span data-ttu-id="b0d75-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="b0d75-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="b0d75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0d75-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d75-103">Obtém um ou mais grupos de máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="b0d75-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="b0d75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0d75-104">SYNTAX</span></span>

### <span data-ttu-id="b0d75-105">ResourceGroupOnly (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0d75-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0d75-106">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="b0d75-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0d75-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="b0d75-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d75-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0d75-108">DESCRIPTION</span></span>
<span data-ttu-id="b0d75-109">O cmdlet Get-AzSqlVMGroup Obtém um ou mais grupos de máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="b0d75-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="b0d75-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0d75-110">EXAMPLES</span></span>

### <span data-ttu-id="b0d75-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b0d75-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="b0d75-112">Esse comando obtém informações sobre todos os grupos de máquinas virtuais do SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b0d75-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="b0d75-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b0d75-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="b0d75-114">Esse comando obtém informações sobre todos os grupos de máquinas virtuais do SQL do Azure na assinatura atual atribuída à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0d75-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="b0d75-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b0d75-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="b0d75-116">Esse comando obtém informações sobre o "grupo de teste" do grupo de máquinas virtuais do SQL atribuída à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0d75-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="b0d75-117">OS</span><span class="sxs-lookup"><span data-stu-id="b0d75-117">PARAMETERS</span></span>

### <span data-ttu-id="b0d75-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d75-118">-DefaultProfile</span></span>
<span data-ttu-id="b0d75-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d75-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d75-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0d75-120">-Name</span></span>
<span data-ttu-id="b0d75-121">Nome do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="b0d75-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="b0d75-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d75-122">-ResourceGroupName</span></span>
<span data-ttu-id="b0d75-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0d75-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="b0d75-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0d75-124">-ResourceId</span></span>
<span data-ttu-id="b0d75-125">ID do recurso de grupo da máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="b0d75-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="b0d75-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d75-126">CommonParameters</span></span>
<span data-ttu-id="b0d75-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d75-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d75-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0d75-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d75-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0d75-129">INPUTS</span></span>

### <span data-ttu-id="b0d75-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b0d75-130">System.String</span></span>

## <span data-ttu-id="b0d75-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0d75-131">OUTPUTS</span></span>

### <span data-ttu-id="b0d75-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b0d75-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="b0d75-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0d75-133">NOTES</span></span>

## <span data-ttu-id="b0d75-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0d75-134">RELATED LINKS</span></span>
