---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111105"
---
# <span data-ttu-id="3dee9-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3dee9-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="3dee9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3dee9-102">SYNOPSIS</span></span>
<span data-ttu-id="3dee9-103">Remove a extensão Diagnóstico de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3dee9-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="3dee9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3dee9-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dee9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3dee9-105">DESCRIPTION</span></span>
<span data-ttu-id="3dee9-106">O cmdlet **Remove-AzVMDiagnosticsExtension** remove uma extensão de Diagnóstico do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3dee9-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="3dee9-107">Você deve passar a saída deste cmdlet para o cmdlet Update-AzVM para implementar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="3dee9-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="3dee9-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3dee9-108">EXAMPLES</span></span>

### <span data-ttu-id="3dee9-109">Exemplo 1: Remover a extensão Diagnóstico de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3dee9-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="3dee9-110">Esse comando remove a extensão diagnóstico de uma máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="3dee9-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="3dee9-111">O comando passa o resultado para o Update-AzVM cmdlet usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="3dee9-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3dee9-112">Esse comando atualiza a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3dee9-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="3dee9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dee9-113">PARAMETERS</span></span>

### <span data-ttu-id="3dee9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dee9-114">-DefaultProfile</span></span>
<span data-ttu-id="3dee9-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3dee9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dee9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dee9-116">-Name</span></span>
<span data-ttu-id="3dee9-117">Especifica o nome da extensão diagnóstico que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="3dee9-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3dee9-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3dee9-118">-NoWait</span></span>
<span data-ttu-id="3dee9-119">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="3dee9-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3dee9-120">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="3dee9-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3dee9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dee9-121">-ResourceGroupName</span></span>
<span data-ttu-id="3dee9-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3dee9-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3dee9-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="3dee9-123">-VMName</span></span>
<span data-ttu-id="3dee9-124">Especifica o nome da máquina virtual da qual este cmdlet remove uma extensão de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="3dee9-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="3dee9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dee9-125">CommonParameters</span></span>
<span data-ttu-id="3dee9-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dee9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dee9-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dee9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dee9-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="3dee9-128">INPUTS</span></span>

### <span data-ttu-id="3dee9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3dee9-129">System.String</span></span>

## <span data-ttu-id="3dee9-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="3dee9-130">OUTPUTS</span></span>

### <span data-ttu-id="3dee9-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3dee9-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3dee9-132">Notas</span><span class="sxs-lookup"><span data-stu-id="3dee9-132">NOTES</span></span>

## <span data-ttu-id="3dee9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3dee9-133">RELATED LINKS</span></span>

[<span data-ttu-id="3dee9-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3dee9-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3dee9-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3dee9-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="3dee9-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3dee9-136">Update-AzVM</span></span>](./Update-AzVM.md)


