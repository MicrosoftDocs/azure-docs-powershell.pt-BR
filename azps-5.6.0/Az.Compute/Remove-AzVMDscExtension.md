---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 30b3ee76a538b4db69e79397bff65e723a9bf908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892534"
---
# <span data-ttu-id="cbdd2-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="cbdd2-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="cbdd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbdd2-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdd2-103">Remove um manipulador de extensão DSC de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="cbdd2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cbdd2-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbdd2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cbdd2-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdd2-106">O cmdlet **Remove-AzVMDscExtension** remove um manipulador de extensão de Configuração de Estado Desejado (DSC) de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="cbdd2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbdd2-107">EXAMPLES</span></span>

### <span data-ttu-id="cbdd2-108">Exemplo 1: Remover uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="cbdd2-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="cbdd2-109">Este comando remove a extensão denominada DSC em uma máquina virtual chamada VM07.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="cbdd2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cbdd2-110">PARAMETERS</span></span>

### <span data-ttu-id="cbdd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdd2-111">-DefaultProfile</span></span>
<span data-ttu-id="cbdd2-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbdd2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cbdd2-113">-Name</span></span>
<span data-ttu-id="cbdd2-114">Especifica o nome da extensão DSC que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="cbdd2-115">O Set-AzVMDscExtension cmdlet define esse nome como Microsoft.Powershell.DSC, que é o valor padrão usado por **Remove-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="cbdd2-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cbdd2-116">-NoWait</span></span>
<span data-ttu-id="cbdd2-117">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cbdd2-118">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cbdd2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbdd2-119">-ResourceGroupName</span></span>
<span data-ttu-id="cbdd2-120">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cbdd2-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="cbdd2-121">-VMName</span></span>
<span data-ttu-id="cbdd2-122">Especifica o nome de uma máquina virtual da qual este cmdlet remove a extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="cbdd2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbdd2-123">-Confirm</span></span>
<span data-ttu-id="cbdd2-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbdd2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbdd2-125">-WhatIf</span></span>
<span data-ttu-id="cbdd2-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbdd2-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbdd2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdd2-128">CommonParameters</span></span>
<span data-ttu-id="cbdd2-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbdd2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdd2-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbdd2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdd2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbdd2-131">INPUTS</span></span>

### <span data-ttu-id="cbdd2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="cbdd2-132">System.String</span></span>

## <span data-ttu-id="cbdd2-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cbdd2-133">OUTPUTS</span></span>

### <span data-ttu-id="cbdd2-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cbdd2-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cbdd2-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="cbdd2-135">NOTES</span></span>

## <span data-ttu-id="cbdd2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbdd2-136">RELATED LINKS</span></span>

[<span data-ttu-id="cbdd2-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="cbdd2-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="cbdd2-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="cbdd2-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


