---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: 4a14c5138a0dac983067e6deb4b1e05b88d85259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433302"
---
# <span data-ttu-id="92170-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="92170-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="92170-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92170-102">SYNOPSIS</span></span>
<span data-ttu-id="92170-103">Remove a extensão de diagnóstico de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="92170-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92170-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92170-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92170-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92170-105">DESCRIPTION</span></span>
<span data-ttu-id="92170-106">O cmdlet **Remove-AzureRmVMDiagnosticsExtension** remove uma extensão de diagnóstico do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="92170-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="92170-107">Você deve passar a saída deste cmdlet para o cmdlet Update-AzureRmVM para implementar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="92170-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="92170-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92170-108">EXAMPLES</span></span>

### <span data-ttu-id="92170-109">Exemplo 1: remover a extensão de diagnóstico de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="92170-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="92170-110">Esse comando Remove a extensão de diagnóstico de uma máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="92170-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="92170-111">O comando passa o resultado para o cmdlet Update-AzureRmVM usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="92170-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="92170-112">Esse comando atualiza a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="92170-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="92170-113">OS</span><span class="sxs-lookup"><span data-stu-id="92170-113">PARAMETERS</span></span>

### <span data-ttu-id="92170-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92170-114">-DefaultProfile</span></span>
<span data-ttu-id="92170-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92170-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92170-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="92170-116">-Name</span></span>
<span data-ttu-id="92170-117">Especifica o nome da extensão do diagnóstico que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="92170-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="92170-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92170-118">-ResourceGroupName</span></span>
<span data-ttu-id="92170-119">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="92170-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="92170-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="92170-120">-VMName</span></span>
<span data-ttu-id="92170-121">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove uma extensão de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="92170-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="92170-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92170-122">CommonParameters</span></span>
<span data-ttu-id="92170-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92170-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92170-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92170-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92170-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92170-125">INPUTS</span></span>

### <span data-ttu-id="92170-126">System. String</span><span class="sxs-lookup"><span data-stu-id="92170-126">System.String</span></span>

## <span data-ttu-id="92170-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92170-127">OUTPUTS</span></span>

### <span data-ttu-id="92170-128">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="92170-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="92170-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92170-129">NOTES</span></span>

## <span data-ttu-id="92170-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92170-130">RELATED LINKS</span></span>

[<span data-ttu-id="92170-131">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="92170-131">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="92170-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="92170-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="92170-133">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92170-133">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


