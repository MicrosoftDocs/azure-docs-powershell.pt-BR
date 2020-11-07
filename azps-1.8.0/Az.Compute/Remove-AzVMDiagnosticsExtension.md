---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bcfc7f3d80c5601d5797d9af2958d2bed6395fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771141"
---
# <span data-ttu-id="b652c-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b652c-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="b652c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b652c-102">SYNOPSIS</span></span>
<span data-ttu-id="b652c-103">Remove a extensão de diagnóstico de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b652c-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="b652c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b652c-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b652c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b652c-105">DESCRIPTION</span></span>
<span data-ttu-id="b652c-106">O cmdlet **Remove-AzVMDiagnosticsExtension** remove uma extensão de diagnóstico do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b652c-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="b652c-107">Você deve passar a saída deste cmdlet para o cmdlet Update-AzVM para implementar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="b652c-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="b652c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b652c-108">EXAMPLES</span></span>

### <span data-ttu-id="b652c-109">Exemplo 1: remover a extensão de diagnóstico de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b652c-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="b652c-110">Esse comando Remove a extensão de diagnóstico de uma máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="b652c-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="b652c-111">O comando passa o resultado para o cmdlet Update-AzVM usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="b652c-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b652c-112">Esse comando atualiza a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b652c-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="b652c-113">OS</span><span class="sxs-lookup"><span data-stu-id="b652c-113">PARAMETERS</span></span>

### <span data-ttu-id="b652c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b652c-114">-DefaultProfile</span></span>
<span data-ttu-id="b652c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b652c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b652c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b652c-116">-Name</span></span>
<span data-ttu-id="b652c-117">Especifica o nome da extensão do diagnóstico que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b652c-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b652c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b652c-118">-ResourceGroupName</span></span>
<span data-ttu-id="b652c-119">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b652c-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b652c-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="b652c-120">-VMName</span></span>
<span data-ttu-id="b652c-121">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove uma extensão de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="b652c-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="b652c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b652c-122">CommonParameters</span></span>
<span data-ttu-id="b652c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b652c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b652c-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b652c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b652c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b652c-125">INPUTS</span></span>

### <span data-ttu-id="b652c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b652c-126">System.String</span></span>

## <span data-ttu-id="b652c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b652c-127">OUTPUTS</span></span>

### <span data-ttu-id="b652c-128">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b652c-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b652c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b652c-129">NOTES</span></span>

## <span data-ttu-id="b652c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b652c-130">RELATED LINKS</span></span>

[<span data-ttu-id="b652c-131">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b652c-131">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="b652c-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b652c-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="b652c-133">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b652c-133">Update-AzVM</span></span>](./Update-AzVM.md)


