---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bec83334032b3d0e18c017bc24d19d381a765176
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776911"
---
# <span data-ttu-id="09147-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="09147-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="09147-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09147-102">SYNOPSIS</span></span>
<span data-ttu-id="09147-103">Remove a extensão de diagnóstico de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="09147-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="09147-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09147-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09147-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09147-105">DESCRIPTION</span></span>
<span data-ttu-id="09147-106">O cmdlet **Remove-AzVMDiagnosticsExtension** remove uma extensão de diagnóstico do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="09147-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="09147-107">Você deve passar a saída deste cmdlet para o cmdlet Update-AzVM para implementar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="09147-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="09147-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09147-108">EXAMPLES</span></span>

### <span data-ttu-id="09147-109">Exemplo 1: remover a extensão de diagnóstico de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="09147-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="09147-110">Esse comando Remove a extensão de diagnóstico de uma máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="09147-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="09147-111">O comando passa o resultado para o cmdlet Update-AzVM usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="09147-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="09147-112">Esse comando atualiza a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="09147-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="09147-113">OS</span><span class="sxs-lookup"><span data-stu-id="09147-113">PARAMETERS</span></span>

### <span data-ttu-id="09147-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09147-114">-DefaultProfile</span></span>
<span data-ttu-id="09147-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09147-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09147-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="09147-116">-Name</span></span>
<span data-ttu-id="09147-117">Especifica o nome da extensão do diagnóstico que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="09147-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="09147-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09147-118">-ResourceGroupName</span></span>
<span data-ttu-id="09147-119">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="09147-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="09147-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="09147-120">-VMName</span></span>
<span data-ttu-id="09147-121">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove uma extensão de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="09147-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="09147-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09147-122">CommonParameters</span></span>
<span data-ttu-id="09147-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09147-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09147-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09147-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09147-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09147-125">INPUTS</span></span>

### <span data-ttu-id="09147-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="09147-126">None</span></span>
<span data-ttu-id="09147-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="09147-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09147-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09147-128">OUTPUTS</span></span>

### <span data-ttu-id="09147-129">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="09147-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="09147-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09147-130">NOTES</span></span>

## <span data-ttu-id="09147-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09147-131">RELATED LINKS</span></span>

[<span data-ttu-id="09147-132">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="09147-132">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="09147-133">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="09147-133">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="09147-134">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="09147-134">Update-AzVM</span></span>](./Update-AzVM.md)


