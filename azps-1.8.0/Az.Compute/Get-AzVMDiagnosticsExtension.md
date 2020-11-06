---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 6b857356ea35476117a58f8f31f7174a7a91767a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601349"
---
# <span data-ttu-id="fe5c9-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fe5c9-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="fe5c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5c9-103">Obtém as configurações da extensão do diagnóstico em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe5c9-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="fe5c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe5c9-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe5c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe5c9-105">DESCRIPTION</span></span>
<span data-ttu-id="fe5c9-106">O cmdlet **Get-AzVMDiagnosticsExtension** Obtém as configurações da extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe5c9-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="fe5c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe5c9-107">EXAMPLES</span></span>

### <span data-ttu-id="fe5c9-108">Exemplo 1: obter a extensão do diagnóstico aplicada a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="fe5c9-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="fe5c9-109">Esse comando obtém a extensão de diagnóstico aplicada à máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="fe5c9-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="fe5c9-110">OS</span><span class="sxs-lookup"><span data-stu-id="fe5c9-110">PARAMETERS</span></span>

### <span data-ttu-id="fe5c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5c9-111">-DefaultProfile</span></span>
<span data-ttu-id="fe5c9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe5c9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe5c9-113">-Name</span></span>
<span data-ttu-id="fe5c9-114">Especifica o nome da extensão do diagnóstico para a qual esse cmdlet obtém configurações.</span><span class="sxs-lookup"><span data-stu-id="fe5c9-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5c9-115">-ResourceGroupName</span></span>
<span data-ttu-id="fe5c9-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe5c9-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c9-117">-Status</span><span class="sxs-lookup"><span data-stu-id="fe5c9-117">-Status</span></span>
<span data-ttu-id="fe5c9-118">Indica que esse cmdlet usa o valor de status.</span><span class="sxs-lookup"><span data-stu-id="fe5c9-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c9-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="fe5c9-119">-VMName</span></span>
<span data-ttu-id="fe5c9-120">Especifica o nome da máquina virtual a partir da qual esse cmdlet obtém a extensão do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="fe5c9-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5c9-121">CommonParameters</span></span>
<span data-ttu-id="fe5c9-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5c9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5c9-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe5c9-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5c9-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe5c9-124">INPUTS</span></span>

### <span data-ttu-id="fe5c9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fe5c9-125">System.String</span></span>

### <span data-ttu-id="fe5c9-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fe5c9-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fe5c9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe5c9-127">OUTPUTS</span></span>

### <span data-ttu-id="fe5c9-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="fe5c9-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="fe5c9-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe5c9-129">NOTES</span></span>

## <span data-ttu-id="fe5c9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe5c9-130">RELATED LINKS</span></span>

[<span data-ttu-id="fe5c9-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fe5c9-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="fe5c9-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="fe5c9-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


