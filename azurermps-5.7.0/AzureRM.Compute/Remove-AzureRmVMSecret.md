---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
ms.openlocfilehash: 84f8abc6c298d7c82bef2494086deef3e4130842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602751"
---
# <span data-ttu-id="8b7fd-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="8b7fd-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="8b7fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b7fd-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7fd-103">Remove (a) segredo (s) de um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8b7fd-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b7fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b7fd-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b7fd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b7fd-105">DESCRIPTION</span></span>
<span data-ttu-id="8b7fd-106">O cmdlet Remove-AzureRmVMSecret Remove (a) segredo (s) de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8b7fd-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="8b7fd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b7fd-107">EXAMPLES</span></span>

### <span data-ttu-id="8b7fd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8b7fd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="8b7fd-109">Remove todos os segredos de uma máquina virtual "VM1" no grupo de recursos "Rg1" e atualiza a VM</span><span class="sxs-lookup"><span data-stu-id="8b7fd-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="8b7fd-110">OS</span><span class="sxs-lookup"><span data-stu-id="8b7fd-110">PARAMETERS</span></span>

### <span data-ttu-id="8b7fd-111">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="8b7fd-111">-SourceVaultId</span></span>
<span data-ttu-id="8b7fd-112">Especifica uma matriz de IDs do cofre de fontes que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8b7fd-112">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7fd-113">-VM</span><span class="sxs-lookup"><span data-stu-id="8b7fd-113">-VM</span></span>
<span data-ttu-id="8b7fd-114">Especifica a máquina virtual a partir da qual esse cmdlet Remove (a) segredo (s).</span><span class="sxs-lookup"><span data-stu-id="8b7fd-114">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="8b7fd-115">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="8b7fd-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7fd-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b7fd-116">-Confirm</span></span>
<span data-ttu-id="8b7fd-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b7fd-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7fd-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b7fd-118">-WhatIf</span></span>
<span data-ttu-id="8b7fd-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b7fd-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b7fd-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b7fd-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7fd-121">CommonParameters</span></span>
<span data-ttu-id="8b7fd-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b7fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7fd-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b7fd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7fd-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b7fd-124">INPUTS</span></span>

### <span data-ttu-id="8b7fd-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8b7fd-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8b7fd-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b7fd-126">OUTPUTS</span></span>

### <span data-ttu-id="8b7fd-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8b7fd-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8b7fd-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b7fd-128">NOTES</span></span>

## <span data-ttu-id="8b7fd-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b7fd-129">RELATED LINKS</span></span>

