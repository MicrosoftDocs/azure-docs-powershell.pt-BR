---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429652"
---
# <span data-ttu-id="7a5cc-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="7a5cc-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="7a5cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5cc-103">Obtém uma ou mais máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="7a5cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a5cc-104">SYNTAX</span></span>

### <span data-ttu-id="7a5cc-105">ResourceGroupOnly (padrão)</span><span class="sxs-lookup"><span data-stu-id="7a5cc-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a5cc-106">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="7a5cc-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a5cc-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="7a5cc-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a5cc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a5cc-108">DESCRIPTION</span></span>
<span data-ttu-id="7a5cc-109">O cmdlet Get-AzSqlVM Obtém uma ou mais máquinas virtuais do SQL.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="7a5cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a5cc-110">EXAMPLES</span></span>

### <span data-ttu-id="7a5cc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a5cc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="7a5cc-112">Esse comando obtém informações sobre todas as máquinas virtuais do Azure SQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="7a5cc-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7a5cc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="7a5cc-114">Esse comando obtém informações sobre todas as máquinas virtuais do Azure SQL na assinatura atual atribuída à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="7a5cc-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7a5cc-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="7a5cc-116">Esse comando obtém informações sobre a máquina virtual do SQL "VM" atribuída à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="7a5cc-117">OS</span><span class="sxs-lookup"><span data-stu-id="7a5cc-117">PARAMETERS</span></span>

### <span data-ttu-id="7a5cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5cc-118">-DefaultProfile</span></span>
<span data-ttu-id="7a5cc-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a5cc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a5cc-120">-Name</span></span>
<span data-ttu-id="7a5cc-121">Nome da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="7a5cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="7a5cc-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a5cc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a5cc-124">-ResourceId</span></span>
<span data-ttu-id="7a5cc-125">ID do recurso da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="7a5cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5cc-126">CommonParameters</span></span>
<span data-ttu-id="7a5cc-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a5cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5cc-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a5cc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5cc-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a5cc-129">INPUTS</span></span>

### <span data-ttu-id="7a5cc-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7a5cc-130">None</span></span>

## <span data-ttu-id="7a5cc-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a5cc-131">OUTPUTS</span></span>

### <span data-ttu-id="7a5cc-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7a5cc-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7a5cc-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a5cc-133">NOTES</span></span>

## <span data-ttu-id="7a5cc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a5cc-134">RELATED LINKS</span></span>
