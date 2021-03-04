---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b3678b52f55e09fdcad8c1d116cd349b2cc5ab45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890554"
---
# <span data-ttu-id="0c9e3-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="0c9e3-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="0c9e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9e3-103">Obtém uma ou mais máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="0c9e3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0c9e3-104">SYNTAX</span></span>

### <span data-ttu-id="0c9e3-105">ResourceGroupOnly (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0c9e3-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c9e3-106">Nome</span><span class="sxs-lookup"><span data-stu-id="0c9e3-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c9e3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c9e3-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c9e3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0c9e3-108">DESCRIPTION</span></span>
<span data-ttu-id="0c9e3-109">O Get-AzSqlVM cmdlet obtém uma ou mais máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="0c9e3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-110">EXAMPLES</span></span>

### <span data-ttu-id="0c9e3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c9e3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="0c9e3-112">Este comando obtém informações sobre todas as máquinas virtuais do Azure SQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="0c9e3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0c9e3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="0c9e3-114">Este comando obtém informações sobre todas as máquinas virtuais do Azure SQL na assinatura atual atribuída ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="0c9e3-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0c9e3-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="0c9e3-116">Este comando obtém informações sobre a SQL "vm" da máquina virtual atribuída ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="0c9e3-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-117">PARAMETERS</span></span>

### <span data-ttu-id="0c9e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9e3-118">-DefaultProfile</span></span>
<span data-ttu-id="0c9e3-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c9e3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0c9e3-120">-Name</span></span>
<span data-ttu-id="0c9e3-121">SQL nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="0c9e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c9e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="0c9e3-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="0c9e3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c9e3-124">-ResourceId</span></span>
<span data-ttu-id="0c9e3-125">SQL id de recurso de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="0c9e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9e3-126">CommonParameters</span></span>
<span data-ttu-id="0c9e3-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c9e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9e3-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c9e3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9e3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-129">INPUTS</span></span>

### <span data-ttu-id="0c9e3-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0c9e3-130">None</span></span>

## <span data-ttu-id="0c9e3-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-131">OUTPUTS</span></span>

### <span data-ttu-id="0c9e3-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="0c9e3-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="0c9e3-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="0c9e3-133">NOTES</span></span>

## <span data-ttu-id="0c9e3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c9e3-134">RELATED LINKS</span></span>
