---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113845"
---
# <span data-ttu-id="e2b9f-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="e2b9f-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="e2b9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b9f-103">Obtém uma ou mais máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="e2b9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2b9f-104">SYNTAX</span></span>

### <span data-ttu-id="e2b9f-105">ResourceGroupOnly (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2b9f-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2b9f-106">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="e2b9f-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2b9f-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="e2b9f-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2b9f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2b9f-108">DESCRIPTION</span></span>
<span data-ttu-id="e2b9f-109">O cmdlet Get-AzSqlVM Obtém uma ou mais máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="e2b9f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2b9f-110">EXAMPLES</span></span>

### <span data-ttu-id="e2b9f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e2b9f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="e2b9f-112">Esse comando obtém informações sobre todas as máquinas virtuais do Azure SQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="e2b9f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e2b9f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="e2b9f-114">Esse comando obtém informações sobre todas as máquinas virtuais do Azure SQL na assinatura atual atribuída à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="e2b9f-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e2b9f-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="e2b9f-116">Esse comando obtém informações sobre a máquina virtual do SQL "VM" atribuída à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e2b9f-117">OS</span><span class="sxs-lookup"><span data-stu-id="e2b9f-117">PARAMETERS</span></span>

### <span data-ttu-id="e2b9f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b9f-118">-DefaultProfile</span></span>
<span data-ttu-id="e2b9f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b9f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2b9f-120">-Name</span></span>
<span data-ttu-id="e2b9f-121">Nome da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="e2b9f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b9f-122">-ResourceGroupName</span></span>
<span data-ttu-id="e2b9f-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2b9f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2b9f-124">-ResourceId</span></span>
<span data-ttu-id="e2b9f-125">ID do recurso da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="e2b9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b9f-126">CommonParameters</span></span>
<span data-ttu-id="e2b9f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b9f-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2b9f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b9f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2b9f-129">INPUTS</span></span>

### <span data-ttu-id="e2b9f-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e2b9f-130">None</span></span>

## <span data-ttu-id="e2b9f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2b9f-131">OUTPUTS</span></span>

### <span data-ttu-id="e2b9f-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="e2b9f-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="e2b9f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2b9f-133">NOTES</span></span>

## <span data-ttu-id="e2b9f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2b9f-134">RELATED LINKS</span></span>
