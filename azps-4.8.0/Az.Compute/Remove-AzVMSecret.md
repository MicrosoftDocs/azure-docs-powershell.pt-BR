---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948108"
---
# <span data-ttu-id="c9395-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="c9395-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="c9395-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9395-102">SYNOPSIS</span></span>
<span data-ttu-id="c9395-103">Remove (a) segredo (s) de um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c9395-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="c9395-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9395-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9395-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9395-105">DESCRIPTION</span></span>
<span data-ttu-id="c9395-106">O cmdlet Remove-AzVMSecret Remove (a) segredo (s) de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9395-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="c9395-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9395-107">EXAMPLES</span></span>

### <span data-ttu-id="c9395-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9395-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="c9395-109">Remove todos os segredos de uma máquina virtual "VM1" no grupo de recursos "Rg1" e atualiza a VM</span><span class="sxs-lookup"><span data-stu-id="c9395-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="c9395-110">OS</span><span class="sxs-lookup"><span data-stu-id="c9395-110">PARAMETERS</span></span>

### <span data-ttu-id="c9395-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9395-111">-DefaultProfile</span></span>
<span data-ttu-id="c9395-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9395-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9395-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="c9395-113">-SourceVaultId</span></span>
<span data-ttu-id="c9395-114">Especifica uma matriz de IDs do cofre de fontes que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c9395-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9395-115">-VM</span><span class="sxs-lookup"><span data-stu-id="c9395-115">-VM</span></span>
<span data-ttu-id="c9395-116">Especifica a máquina virtual a partir da qual esse cmdlet Remove (a) segredo (s).</span><span class="sxs-lookup"><span data-stu-id="c9395-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="c9395-117">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="c9395-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9395-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c9395-118">-Confirm</span></span>
<span data-ttu-id="c9395-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9395-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9395-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9395-120">-WhatIf</span></span>
<span data-ttu-id="c9395-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9395-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9395-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9395-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9395-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9395-123">CommonParameters</span></span>
<span data-ttu-id="c9395-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9395-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9395-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9395-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9395-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9395-126">INPUTS</span></span>

### <span data-ttu-id="c9395-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c9395-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c9395-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9395-128">OUTPUTS</span></span>

### <span data-ttu-id="c9395-129">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c9395-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c9395-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9395-130">NOTES</span></span>

## <span data-ttu-id="c9395-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9395-131">RELATED LINKS</span></span>
