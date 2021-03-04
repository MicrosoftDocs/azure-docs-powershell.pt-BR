---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: e12f69cbb36c5fabccffc4102723175c9f6b8909
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890546"
---
# <span data-ttu-id="782f0-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="782f0-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="782f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="782f0-102">SYNOPSIS</span></span>
<span data-ttu-id="782f0-103">Cria uma nova configuração para uma máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="782f0-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="782f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="782f0-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="782f0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="782f0-105">DESCRIPTION</span></span>
<span data-ttu-id="782f0-106">O New-AzSqlVMConfig cmdlet cria um novo objeto de configuração para uma máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="782f0-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="782f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="782f0-107">EXAMPLES</span></span>

### <span data-ttu-id="782f0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="782f0-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="782f0-109">Cria um objeto configurável local da máquina virtual sql que pode ser usado para criar uma máquina virtual sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="782f0-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="782f0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="782f0-110">PARAMETERS</span></span>

### <span data-ttu-id="782f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782f0-111">-DefaultProfile</span></span>
<span data-ttu-id="782f0-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="782f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="782f0-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="782f0-113">-LicenseType</span></span>
<span data-ttu-id="782f0-114">SQL tipo de licença de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="782f0-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="782f0-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="782f0-115">-Offer</span></span>
<span data-ttu-id="782f0-116">SQL de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="782f0-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="782f0-117">-Sku</span><span class="sxs-lookup"><span data-stu-id="782f0-117">-Sku</span></span>
<span data-ttu-id="782f0-118">SQL tipo de edição de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="782f0-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="782f0-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="782f0-119">-SqlManagementType</span></span>
<span data-ttu-id="782f0-120">SQL tipo de gerenciamento de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="782f0-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="782f0-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="782f0-121">-Tag</span></span>
<span data-ttu-id="782f0-122">As marcas a associar à máquina SQL virtual</span><span class="sxs-lookup"><span data-stu-id="782f0-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="782f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782f0-123">CommonParameters</span></span>
<span data-ttu-id="782f0-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="782f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782f0-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="782f0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782f0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="782f0-126">INPUTS</span></span>

### <span data-ttu-id="782f0-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="782f0-127">None</span></span>

## <span data-ttu-id="782f0-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="782f0-128">OUTPUTS</span></span>

### <span data-ttu-id="782f0-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="782f0-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="782f0-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="782f0-130">NOTES</span></span>

## <span data-ttu-id="782f0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="782f0-131">RELATED LINKS</span></span>
