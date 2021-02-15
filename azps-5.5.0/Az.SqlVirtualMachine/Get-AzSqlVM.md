---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118921"
---
# <span data-ttu-id="3d938-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="3d938-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="3d938-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d938-102">SYNOPSIS</span></span>
<span data-ttu-id="3d938-103">Obtém uma ou mais máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="3d938-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="3d938-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d938-104">SYNTAX</span></span>

### <span data-ttu-id="3d938-105">ResourceGroupOnly (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3d938-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d938-106">Nome</span><span class="sxs-lookup"><span data-stu-id="3d938-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d938-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="3d938-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d938-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d938-108">DESCRIPTION</span></span>
<span data-ttu-id="3d938-109">O Get-AzSqlVM cmdlet obtém uma ou mais máquinas virtuais sql.</span><span class="sxs-lookup"><span data-stu-id="3d938-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="3d938-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3d938-110">EXAMPLES</span></span>

### <span data-ttu-id="3d938-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d938-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="3d938-112">Este comando obtém informações sobre todas as máquinas virtuais SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3d938-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="3d938-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3d938-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="3d938-114">Esse comando obtém informações sobre todas as máquinas virtuais SQL do Azure na assinatura atual atribuída ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3d938-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="3d938-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3d938-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="3d938-116">Esse comando obtém informações sobre o "vm" da máquina virtual SQL atribuída ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3d938-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="3d938-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d938-117">PARAMETERS</span></span>

### <span data-ttu-id="3d938-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d938-118">-DefaultProfile</span></span>
<span data-ttu-id="3d938-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d938-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d938-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d938-120">-Name</span></span>
<span data-ttu-id="3d938-121">Nome da máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="3d938-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="3d938-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d938-122">-ResourceGroupName</span></span>
<span data-ttu-id="3d938-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d938-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="3d938-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d938-124">-ResourceId</span></span>
<span data-ttu-id="3d938-125">ID do recurso de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="3d938-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="3d938-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d938-126">CommonParameters</span></span>
<span data-ttu-id="3d938-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d938-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d938-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d938-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d938-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="3d938-129">INPUTS</span></span>

### <span data-ttu-id="3d938-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3d938-130">None</span></span>

## <span data-ttu-id="3d938-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="3d938-131">OUTPUTS</span></span>

### <span data-ttu-id="3d938-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="3d938-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="3d938-133">Notas</span><span class="sxs-lookup"><span data-stu-id="3d938-133">NOTES</span></span>

## <span data-ttu-id="3d938-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d938-134">RELATED LINKS</span></span>
