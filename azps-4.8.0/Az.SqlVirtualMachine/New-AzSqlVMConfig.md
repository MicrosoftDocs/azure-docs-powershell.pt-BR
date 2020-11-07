---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954551"
---
# <span data-ttu-id="a5726-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="a5726-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="a5726-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5726-102">SYNOPSIS</span></span>
<span data-ttu-id="a5726-103">Cria uma nova configuração para uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="a5726-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="a5726-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5726-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5726-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5726-105">DESCRIPTION</span></span>
<span data-ttu-id="a5726-106">O cmdlet New-AzSqlVMConfig cria um novo objeto de configuração para uma máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="a5726-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="a5726-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5726-107">EXAMPLES</span></span>

### <span data-ttu-id="a5726-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5726-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="a5726-109">Cria um objeto configurável local da máquina virtual SQL que pode ser usado para criar uma máquina virtual do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a5726-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="a5726-110">OS</span><span class="sxs-lookup"><span data-stu-id="a5726-110">PARAMETERS</span></span>

### <span data-ttu-id="a5726-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5726-111">-DefaultProfile</span></span>
<span data-ttu-id="a5726-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5726-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5726-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a5726-113">-LicenseType</span></span>
<span data-ttu-id="a5726-114">Tipo de licença da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="a5726-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="a5726-115">-Oferta</span><span class="sxs-lookup"><span data-stu-id="a5726-115">-Offer</span></span>
<span data-ttu-id="a5726-116">Oferta da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="a5726-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="a5726-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="a5726-117">-Sku</span></span>
<span data-ttu-id="a5726-118">Tipo de edição da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="a5726-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="a5726-119">-Sqlmanagementtype</span><span class="sxs-lookup"><span data-stu-id="a5726-119">-SqlManagementType</span></span>
<span data-ttu-id="a5726-120">Tipo de gerenciamento da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="a5726-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="a5726-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="a5726-121">-Tag</span></span>
<span data-ttu-id="a5726-122">As marcas a serem associadas à máquina virtual do SQL</span><span class="sxs-lookup"><span data-stu-id="a5726-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="a5726-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5726-123">CommonParameters</span></span>
<span data-ttu-id="a5726-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5726-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5726-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5726-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5726-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5726-126">INPUTS</span></span>

### <span data-ttu-id="a5726-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a5726-127">None</span></span>

## <span data-ttu-id="a5726-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5726-128">OUTPUTS</span></span>

### <span data-ttu-id="a5726-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="a5726-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a5726-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5726-130">NOTES</span></span>

## <span data-ttu-id="a5726-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5726-131">RELATED LINKS</span></span>
