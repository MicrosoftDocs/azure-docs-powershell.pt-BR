---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 57e3aef7ff5b6acece0ccba1505d33f2add05ae2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785981"
---
# <span data-ttu-id="da1a2-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="da1a2-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="da1a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="da1a2-103">Remove a extensão de diagnóstico de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="da1a2-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da1a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da1a2-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da1a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da1a2-105">DESCRIPTION</span></span>
<span data-ttu-id="da1a2-106">O cmdlet **Remove-AzureRmVMDiagnosticsExtension** remove uma extensão de diagnóstico do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="da1a2-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="da1a2-107">Você deve passar a saída deste cmdlet para o cmdlet Update-AzureRmVM para implementar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="da1a2-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="da1a2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da1a2-108">EXAMPLES</span></span>

### <span data-ttu-id="da1a2-109">Exemplo 1: remover a extensão de diagnóstico de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="da1a2-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="da1a2-110">Esse comando Remove a extensão de diagnóstico de uma máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="da1a2-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="da1a2-111">O comando passa o resultado para o cmdlet Update-AzureRmVM usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="da1a2-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="da1a2-112">Esse comando atualiza a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="da1a2-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="da1a2-113">OS</span><span class="sxs-lookup"><span data-stu-id="da1a2-113">PARAMETERS</span></span>

### <span data-ttu-id="da1a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1a2-114">-DefaultProfile</span></span>
<span data-ttu-id="da1a2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da1a2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da1a2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="da1a2-116">-Name</span></span>
<span data-ttu-id="da1a2-117">Especifica o nome da extensão do diagnóstico que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="da1a2-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="da1a2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da1a2-118">-ResourceGroupName</span></span>
<span data-ttu-id="da1a2-119">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="da1a2-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="da1a2-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="da1a2-120">-VMName</span></span>
<span data-ttu-id="da1a2-121">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove uma extensão de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="da1a2-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="da1a2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1a2-122">CommonParameters</span></span>
<span data-ttu-id="da1a2-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da1a2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1a2-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da1a2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1a2-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da1a2-125">INPUTS</span></span>

### <span data-ttu-id="da1a2-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="da1a2-126">None</span></span>
<span data-ttu-id="da1a2-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="da1a2-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da1a2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da1a2-128">OUTPUTS</span></span>

### <span data-ttu-id="da1a2-129">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="da1a2-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="da1a2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da1a2-130">NOTES</span></span>

## <span data-ttu-id="da1a2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da1a2-131">RELATED LINKS</span></span>

[<span data-ttu-id="da1a2-132">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="da1a2-132">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="da1a2-133">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="da1a2-133">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="da1a2-134">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="da1a2-134">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


