---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111103"
---
# <span data-ttu-id="c93d2-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c93d2-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="c93d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c93d2-102">SYNOPSIS</span></span>
<span data-ttu-id="c93d2-103">Remove um manipulador de extensão DSC de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c93d2-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="c93d2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c93d2-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c93d2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c93d2-105">DESCRIPTION</span></span>
<span data-ttu-id="c93d2-106">O cmdlet **Remove-AzVMDscExtension** remove um manipulador de extensão de Configuração de Estado Desejado (DSC) de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c93d2-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="c93d2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c93d2-107">EXAMPLES</span></span>

### <span data-ttu-id="c93d2-108">Exemplo 1: Remover uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="c93d2-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="c93d2-109">Esse comando remove a extensão chamada DSC em uma máquina virtual chamada VM07.</span><span class="sxs-lookup"><span data-stu-id="c93d2-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="c93d2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c93d2-110">PARAMETERS</span></span>

### <span data-ttu-id="c93d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93d2-111">-DefaultProfile</span></span>
<span data-ttu-id="c93d2-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c93d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c93d2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c93d2-113">-Name</span></span>
<span data-ttu-id="c93d2-114">Especifica o nome da extensão DSC que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="c93d2-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="c93d2-115">O Set-AzVMDscExtension cmdlet define esse nome para Microsoft.Powershell.DSC, que é o valor padrão usado por **Remove-AzVMDscExtension.**</span><span class="sxs-lookup"><span data-stu-id="c93d2-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c93d2-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c93d2-116">-NoWait</span></span>
<span data-ttu-id="c93d2-117">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="c93d2-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c93d2-118">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="c93d2-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c93d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c93d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="c93d2-120">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c93d2-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c93d2-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="c93d2-121">-VMName</span></span>
<span data-ttu-id="c93d2-122">Especifica o nome de uma máquina virtual da qual este cmdlet remove a extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="c93d2-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c93d2-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c93d2-123">-Confirm</span></span>
<span data-ttu-id="c93d2-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c93d2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c93d2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c93d2-125">-WhatIf</span></span>
<span data-ttu-id="c93d2-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c93d2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c93d2-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c93d2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c93d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93d2-128">CommonParameters</span></span>
<span data-ttu-id="c93d2-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93d2-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c93d2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93d2-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="c93d2-131">INPUTS</span></span>

### <span data-ttu-id="c93d2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c93d2-132">System.String</span></span>

## <span data-ttu-id="c93d2-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="c93d2-133">OUTPUTS</span></span>

### <span data-ttu-id="c93d2-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c93d2-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c93d2-135">Notas</span><span class="sxs-lookup"><span data-stu-id="c93d2-135">NOTES</span></span>

## <span data-ttu-id="c93d2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c93d2-136">RELATED LINKS</span></span>

[<span data-ttu-id="c93d2-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c93d2-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="c93d2-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c93d2-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


