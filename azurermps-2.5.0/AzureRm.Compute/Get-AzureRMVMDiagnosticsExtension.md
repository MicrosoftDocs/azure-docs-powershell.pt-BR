---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: e02c86407326d9ea5b12a5a589e5860c9dfb5c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786578"
---
# <span data-ttu-id="a249a-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a249a-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a249a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a249a-102">SYNOPSIS</span></span>
<span data-ttu-id="a249a-103">Obtém as configurações da extensão do diagnóstico em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a249a-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a249a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a249a-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a249a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a249a-105">DESCRIPTION</span></span>
<span data-ttu-id="a249a-106">O cmdlet **Get-AzureRmVMDiagnosticsExtension** Obtém as configurações da extensão de diagnóstico do Azure em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a249a-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a249a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a249a-107">EXAMPLES</span></span>

### <span data-ttu-id="a249a-108">Exemplo 1: obter a extensão do diagnóstico aplicada a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="a249a-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="a249a-109">Esse comando obtém a extensão de diagnóstico aplicada à máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="a249a-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="a249a-110">OS</span><span class="sxs-lookup"><span data-stu-id="a249a-110">PARAMETERS</span></span>

### <span data-ttu-id="a249a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a249a-111">-DefaultProfile</span></span>
<span data-ttu-id="a249a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a249a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a249a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a249a-113">-Name</span></span>
<span data-ttu-id="a249a-114">Especifica o nome da extensão do diagnóstico para a qual esse cmdlet obtém configurações.</span><span class="sxs-lookup"><span data-stu-id="a249a-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="a249a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a249a-115">-ResourceGroupName</span></span>
<span data-ttu-id="a249a-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a249a-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a249a-117">-Status</span><span class="sxs-lookup"><span data-stu-id="a249a-117">-Status</span></span>
<span data-ttu-id="a249a-118">Indica que esse cmdlet usa o valor de status.</span><span class="sxs-lookup"><span data-stu-id="a249a-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="a249a-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="a249a-119">-VMName</span></span>
<span data-ttu-id="a249a-120">Especifica o nome da máquina virtual a partir da qual esse cmdlet obtém a extensão do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a249a-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="a249a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a249a-121">CommonParameters</span></span>
<span data-ttu-id="a249a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a249a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a249a-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a249a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a249a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a249a-124">INPUTS</span></span>

### <span data-ttu-id="a249a-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a249a-125">None</span></span>
<span data-ttu-id="a249a-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a249a-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a249a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a249a-127">OUTPUTS</span></span>

### <span data-ttu-id="a249a-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a249a-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="a249a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a249a-129">NOTES</span></span>

## <span data-ttu-id="a249a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a249a-130">RELATED LINKS</span></span>

[<span data-ttu-id="a249a-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a249a-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="a249a-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a249a-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


