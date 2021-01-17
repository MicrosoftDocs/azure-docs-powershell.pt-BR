---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434254"
---
# <span data-ttu-id="16757-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="16757-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="16757-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16757-102">SYNOPSIS</span></span>
<span data-ttu-id="16757-103">Remove a extensão de diagnóstico de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="16757-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="16757-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16757-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16757-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16757-105">DESCRIPTION</span></span>
<span data-ttu-id="16757-106">O cmdlet **Remove-AzVMDiagnosticsExtension** remove uma extensão de diagnóstico do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="16757-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="16757-107">Você deve passar a saída deste cmdlet para o cmdlet Update-AzVM para implementar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="16757-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="16757-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16757-108">EXAMPLES</span></span>

### <span data-ttu-id="16757-109">Exemplo 1: remover a extensão de diagnóstico de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="16757-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="16757-110">Esse comando Remove a extensão de diagnóstico de uma máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="16757-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="16757-111">O comando passa o resultado para o cmdlet Update-AzVM usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="16757-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="16757-112">Esse comando atualiza a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="16757-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="16757-113">OS</span><span class="sxs-lookup"><span data-stu-id="16757-113">PARAMETERS</span></span>

### <span data-ttu-id="16757-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16757-114">-DefaultProfile</span></span>
<span data-ttu-id="16757-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16757-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16757-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="16757-116">-Name</span></span>
<span data-ttu-id="16757-117">Especifica o nome da extensão do diagnóstico que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="16757-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16757-118">-Nowait</span><span class="sxs-lookup"><span data-stu-id="16757-118">-NoWait</span></span>
<span data-ttu-id="16757-119">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="16757-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="16757-120">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="16757-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16757-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16757-121">-ResourceGroupName</span></span>
<span data-ttu-id="16757-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="16757-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="16757-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="16757-123">-VMName</span></span>
<span data-ttu-id="16757-124">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove uma extensão de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="16757-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="16757-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16757-125">CommonParameters</span></span>
<span data-ttu-id="16757-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16757-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16757-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16757-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16757-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16757-128">INPUTS</span></span>

### <span data-ttu-id="16757-129">System. String</span><span class="sxs-lookup"><span data-stu-id="16757-129">System.String</span></span>

## <span data-ttu-id="16757-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16757-130">OUTPUTS</span></span>

### <span data-ttu-id="16757-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="16757-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="16757-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16757-132">NOTES</span></span>

## <span data-ttu-id="16757-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16757-133">RELATED LINKS</span></span>

[<span data-ttu-id="16757-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="16757-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="16757-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="16757-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="16757-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="16757-136">Update-AzVM</span></span>](./Update-AzVM.md)


