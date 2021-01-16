---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429646"
---
# <span data-ttu-id="1cfd9-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="1cfd9-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="1cfd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cfd9-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfd9-103">Cria uma nova configuração para uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="1cfd9-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="1cfd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cfd9-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cfd9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cfd9-105">DESCRIPTION</span></span>
<span data-ttu-id="1cfd9-106">O cmdlet New-AzSqlVMConfig cria um novo objeto de configuração para uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="1cfd9-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="1cfd9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cfd9-107">EXAMPLES</span></span>

### <span data-ttu-id="1cfd9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1cfd9-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="1cfd9-109">Cria um objeto configurável local da máquina virtual SQL que pode ser usado para criar uma máquina virtual do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1cfd9-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="1cfd9-110">OS</span><span class="sxs-lookup"><span data-stu-id="1cfd9-110">PARAMETERS</span></span>

### <span data-ttu-id="1cfd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfd9-111">-DefaultProfile</span></span>
<span data-ttu-id="1cfd9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cfd9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cfd9-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1cfd9-113">-LicenseType</span></span>
<span data-ttu-id="1cfd9-114">Tipo de licença da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="1cfd9-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="1cfd9-115">-Oferta</span><span class="sxs-lookup"><span data-stu-id="1cfd9-115">-Offer</span></span>
<span data-ttu-id="1cfd9-116">Oferta da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="1cfd9-116">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cfd9-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="1cfd9-117">-Sku</span></span>
<span data-ttu-id="1cfd9-118">Tipo de edição da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="1cfd9-118">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cfd9-119">-Sqlmanagementtype</span><span class="sxs-lookup"><span data-stu-id="1cfd9-119">-SqlManagementType</span></span>
<span data-ttu-id="1cfd9-120">Tipo de gerenciamento da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="1cfd9-120">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cfd9-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="1cfd9-121">-Tag</span></span>
<span data-ttu-id="1cfd9-122">As marcas a serem associadas à máquina virtual do SQL</span><span class="sxs-lookup"><span data-stu-id="1cfd9-122">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cfd9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfd9-123">CommonParameters</span></span>
<span data-ttu-id="1cfd9-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cfd9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfd9-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cfd9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfd9-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cfd9-126">INPUTS</span></span>

### <span data-ttu-id="1cfd9-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1cfd9-127">None</span></span>

## <span data-ttu-id="1cfd9-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cfd9-128">OUTPUTS</span></span>

### <span data-ttu-id="1cfd9-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="1cfd9-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="1cfd9-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cfd9-130">NOTES</span></span>

## <span data-ttu-id="1cfd9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cfd9-131">RELATED LINKS</span></span>
