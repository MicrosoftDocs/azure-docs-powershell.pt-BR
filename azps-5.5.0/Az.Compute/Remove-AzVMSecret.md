---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117844"
---
# <span data-ttu-id="9f536-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="9f536-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="9f536-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f536-102">SYNOPSIS</span></span>
<span data-ttu-id="9f536-103">Remove (a) segredo(s) de um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="9f536-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="9f536-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f536-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f536-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f536-105">DESCRIPTION</span></span>
<span data-ttu-id="9f536-106">O Remove-AzVMSecret cmdlet remove (a) segredo(s) de um objeto virtual de máquina.</span><span class="sxs-lookup"><span data-stu-id="9f536-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="9f536-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f536-107">EXAMPLES</span></span>

### <span data-ttu-id="9f536-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f536-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="9f536-109">Remove todos os segredos de uma máquina virtual "vm1" no grupo de recursos "rg1" e atualiza o VM</span><span class="sxs-lookup"><span data-stu-id="9f536-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="9f536-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f536-110">PARAMETERS</span></span>

### <span data-ttu-id="9f536-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f536-111">-DefaultProfile</span></span>
<span data-ttu-id="9f536-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9f536-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f536-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="9f536-113">-SourceVaultId</span></span>
<span data-ttu-id="9f536-114">Especifica uma matriz de IDs do cofre de origem que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="9f536-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9f536-115">-VM</span><span class="sxs-lookup"><span data-stu-id="9f536-115">-VM</span></span>
<span data-ttu-id="9f536-116">Especifica a máquina virtual da qual este cmdlet remove (a) segredo(s).</span><span class="sxs-lookup"><span data-stu-id="9f536-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="9f536-117">Para obter um objeto virtual de máquina, use o cmdlet Get-AzVM computador.</span><span class="sxs-lookup"><span data-stu-id="9f536-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="9f536-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9f536-118">-Confirm</span></span>
<span data-ttu-id="9f536-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f536-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f536-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f536-120">-WhatIf</span></span>
<span data-ttu-id="9f536-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9f536-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f536-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f536-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f536-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f536-123">CommonParameters</span></span>
<span data-ttu-id="9f536-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f536-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f536-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f536-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f536-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f536-126">INPUTS</span></span>

### <span data-ttu-id="9f536-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9f536-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9f536-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f536-128">OUTPUTS</span></span>

### <span data-ttu-id="9f536-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9f536-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9f536-130">Notas</span><span class="sxs-lookup"><span data-stu-id="9f536-130">NOTES</span></span>

## <span data-ttu-id="9f536-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f536-131">RELATED LINKS</span></span>
