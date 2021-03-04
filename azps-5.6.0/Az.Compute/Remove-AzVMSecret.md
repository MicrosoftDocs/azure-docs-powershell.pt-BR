---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 794447801789bd8923012c19914ee41e736fb945
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889557"
---
# <span data-ttu-id="38a35-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="38a35-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="38a35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38a35-102">SYNOPSIS</span></span>
<span data-ttu-id="38a35-103">Remove (a) secret(s) de um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="38a35-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="38a35-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38a35-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38a35-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38a35-105">DESCRIPTION</span></span>
<span data-ttu-id="38a35-106">O Remove-AzVMSecret cmdlet remove (a) segredo(s) de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="38a35-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="38a35-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38a35-107">EXAMPLES</span></span>

### <span data-ttu-id="38a35-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38a35-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="38a35-109">Remove todos os segredos de uma máquina virtual "vm1" no grupo de recursos "rg1" e atualiza a VM</span><span class="sxs-lookup"><span data-stu-id="38a35-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="38a35-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38a35-110">PARAMETERS</span></span>

### <span data-ttu-id="38a35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a35-111">-DefaultProfile</span></span>
<span data-ttu-id="38a35-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="38a35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38a35-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="38a35-113">-SourceVaultId</span></span>
<span data-ttu-id="38a35-114">Especifica uma matriz de IDs do cofre de origem que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="38a35-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38a35-115">-VM</span><span class="sxs-lookup"><span data-stu-id="38a35-115">-VM</span></span>
<span data-ttu-id="38a35-116">Especifica a máquina virtual da qual esse cmdlet remove (a) segredo(s).</span><span class="sxs-lookup"><span data-stu-id="38a35-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="38a35-117">Para obter um objeto de máquina virtual, use Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a35-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="38a35-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38a35-118">-Confirm</span></span>
<span data-ttu-id="38a35-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a35-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38a35-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a35-120">-WhatIf</span></span>
<span data-ttu-id="38a35-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38a35-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38a35-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38a35-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38a35-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a35-123">CommonParameters</span></span>
<span data-ttu-id="38a35-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a35-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a35-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38a35-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a35-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38a35-126">INPUTS</span></span>

### <span data-ttu-id="38a35-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="38a35-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="38a35-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38a35-128">OUTPUTS</span></span>

### <span data-ttu-id="38a35-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="38a35-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="38a35-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="38a35-130">NOTES</span></span>

## <span data-ttu-id="38a35-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38a35-131">RELATED LINKS</span></span>
