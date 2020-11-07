---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9137b62098a1441cea8acc53c52c0e0ea835ff09
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777032"
---
# <span data-ttu-id="6c5d1-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6c5d1-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="6c5d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5d1-103">Obtém as configurações da extensão do diagnóstico em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="6c5d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c5d1-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c5d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c5d1-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5d1-106">O cmdlet **Get-AzVMDiagnosticsExtension** Obtém as configurações da extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="6c5d1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c5d1-107">EXAMPLES</span></span>

### <span data-ttu-id="6c5d1-108">Exemplo 1: obter a extensão do diagnóstico aplicada a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="6c5d1-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="6c5d1-109">Esse comando obtém a extensão de diagnóstico aplicada à máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="6c5d1-110">OS</span><span class="sxs-lookup"><span data-stu-id="6c5d1-110">PARAMETERS</span></span>

### <span data-ttu-id="6c5d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5d1-111">-DefaultProfile</span></span>
<span data-ttu-id="6c5d1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5d1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c5d1-113">-Name</span></span>
<span data-ttu-id="6c5d1-114">Especifica o nome da extensão do diagnóstico para a qual esse cmdlet obtém configurações.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c5d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="6c5d1-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5d1-117">-Status</span><span class="sxs-lookup"><span data-stu-id="6c5d1-117">-Status</span></span>
<span data-ttu-id="6c5d1-118">Indica que esse cmdlet usa o valor de status.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5d1-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="6c5d1-119">-VMName</span></span>
<span data-ttu-id="6c5d1-120">Especifica o nome da máquina virtual a partir da qual esse cmdlet obtém a extensão do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5d1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5d1-121">CommonParameters</span></span>
<span data-ttu-id="6c5d1-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5d1-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c5d1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5d1-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c5d1-124">INPUTS</span></span>

### <span data-ttu-id="6c5d1-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6c5d1-125">None</span></span>
<span data-ttu-id="6c5d1-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6c5d1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6c5d1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c5d1-127">OUTPUTS</span></span>

### <span data-ttu-id="6c5d1-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6c5d1-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="6c5d1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c5d1-129">NOTES</span></span>

## <span data-ttu-id="6c5d1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c5d1-130">RELATED LINKS</span></span>

[<span data-ttu-id="6c5d1-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6c5d1-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="6c5d1-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6c5d1-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


