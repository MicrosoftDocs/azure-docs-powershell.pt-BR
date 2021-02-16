---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118594"
---
# <span data-ttu-id="02e74-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="02e74-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="02e74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02e74-102">SYNOPSIS</span></span>
<span data-ttu-id="02e74-103">Cria uma nova configuração para uma máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="02e74-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="02e74-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02e74-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02e74-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="02e74-105">DESCRIPTION</span></span>
<span data-ttu-id="02e74-106">O New-AzSqlVMConfig cmdlet cria um novo objeto de configuração para uma máquina virtual sql.</span><span class="sxs-lookup"><span data-stu-id="02e74-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="02e74-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="02e74-107">EXAMPLES</span></span>

### <span data-ttu-id="02e74-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02e74-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="02e74-109">Cria um objeto configurável local de uma máquina virtual sql que pode ser usada para criar uma máquina virtual sql do Azure.</span><span class="sxs-lookup"><span data-stu-id="02e74-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="02e74-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02e74-110">PARAMETERS</span></span>

### <span data-ttu-id="02e74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e74-111">-DefaultProfile</span></span>
<span data-ttu-id="02e74-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02e74-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02e74-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="02e74-113">-LicenseType</span></span>
<span data-ttu-id="02e74-114">Tipo de licença de computador virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="02e74-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="02e74-115">-Oferta</span><span class="sxs-lookup"><span data-stu-id="02e74-115">-Offer</span></span>
<span data-ttu-id="02e74-116">Oferta de computador virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="02e74-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="02e74-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="02e74-117">-Sku</span></span>
<span data-ttu-id="02e74-118">Tipo de edição de computador virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="02e74-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="02e74-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="02e74-119">-SqlManagementType</span></span>
<span data-ttu-id="02e74-120">Tipo de gerenciamento de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="02e74-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="02e74-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="02e74-121">-Tag</span></span>
<span data-ttu-id="02e74-122">As marcas a associar à máquina virtual SQL</span><span class="sxs-lookup"><span data-stu-id="02e74-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="02e74-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e74-123">CommonParameters</span></span>
<span data-ttu-id="02e74-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02e74-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e74-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02e74-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e74-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="02e74-126">INPUTS</span></span>

### <span data-ttu-id="02e74-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="02e74-127">None</span></span>

## <span data-ttu-id="02e74-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="02e74-128">OUTPUTS</span></span>

### <span data-ttu-id="02e74-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="02e74-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="02e74-130">Notas</span><span class="sxs-lookup"><span data-stu-id="02e74-130">NOTES</span></span>

## <span data-ttu-id="02e74-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02e74-131">RELATED LINKS</span></span>
