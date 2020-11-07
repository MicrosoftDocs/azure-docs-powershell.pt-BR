---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: da904e6dfbf9d85319636b3bc6ff5ced5f0b2973
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776903"
---
# <span data-ttu-id="b6ab3-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="b6ab3-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="b6ab3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ab3-103">Remove (a) segredo (s) de um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b6ab3-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="b6ab3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6ab3-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6ab3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ab3-106">O cmdlet Remove-AzVMSecret Remove (a) segredo (s) de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b6ab3-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="b6ab3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="b6ab3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6ab3-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="b6ab3-109">Remove todos os segredos de uma máquina virtual "VM1" no grupo de recursos "Rg1" e atualiza a VM</span><span class="sxs-lookup"><span data-stu-id="b6ab3-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="b6ab3-110">OS</span><span class="sxs-lookup"><span data-stu-id="b6ab3-110">PARAMETERS</span></span>

### <span data-ttu-id="b6ab3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ab3-111">-DefaultProfile</span></span>
<span data-ttu-id="b6ab3-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ab3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6ab3-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b6ab3-113">-SourceVaultId</span></span>
<span data-ttu-id="b6ab3-114">Especifica uma matriz de IDs do cofre de fontes que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b6ab3-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6ab3-115">-VM</span><span class="sxs-lookup"><span data-stu-id="b6ab3-115">-VM</span></span>
<span data-ttu-id="b6ab3-116">Especifica a máquina virtual a partir da qual esse cmdlet Remove (a) segredo (s).</span><span class="sxs-lookup"><span data-stu-id="b6ab3-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="b6ab3-117">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="b6ab3-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="b6ab3-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6ab3-118">-Confirm</span></span>
<span data-ttu-id="b6ab3-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6ab3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6ab3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ab3-120">-WhatIf</span></span>
<span data-ttu-id="b6ab3-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6ab3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6ab3-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6ab3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6ab3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ab3-123">CommonParameters</span></span>
<span data-ttu-id="b6ab3-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ab3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ab3-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ab3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ab3-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6ab3-126">INPUTS</span></span>

### <span data-ttu-id="b6ab3-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b6ab3-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b6ab3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6ab3-128">OUTPUTS</span></span>

### <span data-ttu-id="b6ab3-129">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b6ab3-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b6ab3-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6ab3-130">NOTES</span></span>

## <span data-ttu-id="b6ab3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6ab3-131">RELATED LINKS</span></span>

