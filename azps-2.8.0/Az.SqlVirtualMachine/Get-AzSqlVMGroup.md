---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: 1d6c7ef54248258fc6a641dc6c917866163bd52a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773971"
---
# <span data-ttu-id="a5adb-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="a5adb-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="a5adb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5adb-102">SYNOPSIS</span></span>
<span data-ttu-id="a5adb-103">Obtém um ou mais grupos de máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="a5adb-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="a5adb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5adb-104">SYNTAX</span></span>

### <span data-ttu-id="a5adb-105">ResourceGroupOnly (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5adb-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5adb-106">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="a5adb-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5adb-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="a5adb-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5adb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5adb-108">DESCRIPTION</span></span>
<span data-ttu-id="a5adb-109">O cmdlet Get-AzSqlVMGroup Obtém um ou mais grupos de máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="a5adb-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="a5adb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5adb-110">EXAMPLES</span></span>

### <span data-ttu-id="a5adb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5adb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="a5adb-112">Esse comando obtém informações sobre todos os grupos de máquinas virtuais do SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a5adb-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="a5adb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a5adb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="a5adb-114">Esse comando obtém informações sobre todos os grupos de máquinas virtuais do SQL do Azure na assinatura atual atribuída à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a5adb-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a5adb-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a5adb-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="a5adb-116">Esse comando obtém informações sobre o "grupo de teste" do grupo de máquinas virtuais do SQL atribuída à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a5adb-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="a5adb-117">OS</span><span class="sxs-lookup"><span data-stu-id="a5adb-117">PARAMETERS</span></span>

### <span data-ttu-id="a5adb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5adb-118">-DefaultProfile</span></span>
<span data-ttu-id="a5adb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5adb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5adb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5adb-120">-Name</span></span>
<span data-ttu-id="a5adb-121">Nome do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="a5adb-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="a5adb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5adb-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5adb-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a5adb-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5adb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5adb-124">-ResourceId</span></span>
<span data-ttu-id="a5adb-125">ID do recurso de grupo da máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="a5adb-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="a5adb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5adb-126">CommonParameters</span></span>
<span data-ttu-id="a5adb-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5adb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5adb-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5adb-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5adb-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5adb-129">INPUTS</span></span>

### <span data-ttu-id="a5adb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a5adb-130">System.String</span></span>

## <span data-ttu-id="a5adb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5adb-131">OUTPUTS</span></span>

### <span data-ttu-id="a5adb-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="a5adb-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="a5adb-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5adb-133">NOTES</span></span>

## <span data-ttu-id="a5adb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5adb-134">RELATED LINKS</span></span>
