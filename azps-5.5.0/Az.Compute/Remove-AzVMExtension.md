---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111102"
---
# <span data-ttu-id="1498f-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1498f-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="1498f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1498f-102">SYNOPSIS</span></span>
<span data-ttu-id="1498f-103">Remove uma extensão de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1498f-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="1498f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1498f-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1498f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1498f-105">DESCRIPTION</span></span>
<span data-ttu-id="1498f-106">O **cmdlet Remove-AzVMExtension** remove uma extensão das Extensões de Máquina Virtual de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1498f-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="1498f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1498f-107">EXAMPLES</span></span>

### <span data-ttu-id="1498f-108">Exemplo 1: Remover uma extensão de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="1498f-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="1498f-109">Esse comando remove a extensão chamada ContosoTest da máquina virtual chamada VirtualMachine22 no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1498f-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="1498f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1498f-110">PARAMETERS</span></span>

### <span data-ttu-id="1498f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1498f-111">-DefaultProfile</span></span>
<span data-ttu-id="1498f-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1498f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1498f-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1498f-113">-Force</span></span>
<span data-ttu-id="1498f-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1498f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1498f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1498f-115">-Name</span></span>
<span data-ttu-id="1498f-116">Especifica o nome da extensão que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="1498f-116">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1498f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1498f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1498f-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1498f-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1498f-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="1498f-119">-VMName</span></span>
<span data-ttu-id="1498f-120">Especifica o nome de uma máquina virtual da qual este cmdlet remove a extensão.</span><span class="sxs-lookup"><span data-stu-id="1498f-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="1498f-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1498f-121">-Confirm</span></span>
<span data-ttu-id="1498f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1498f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1498f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1498f-123">-WhatIf</span></span>
<span data-ttu-id="1498f-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1498f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1498f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1498f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1498f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1498f-126">CommonParameters</span></span>
<span data-ttu-id="1498f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1498f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1498f-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1498f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1498f-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="1498f-129">INPUTS</span></span>

### <span data-ttu-id="1498f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1498f-130">System.String</span></span>

## <span data-ttu-id="1498f-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="1498f-131">OUTPUTS</span></span>

### <span data-ttu-id="1498f-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1498f-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1498f-133">Notas</span><span class="sxs-lookup"><span data-stu-id="1498f-133">NOTES</span></span>

## <span data-ttu-id="1498f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1498f-134">RELATED LINKS</span></span>

[<span data-ttu-id="1498f-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1498f-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="1498f-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1498f-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


