---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 56973d23e59a3d34b2caadce3677ca0bfd5f3c5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888000"
---
# <span data-ttu-id="3db66-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3db66-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="3db66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3db66-102">SYNOPSIS</span></span>
<span data-ttu-id="3db66-103">Remove a extensão do Chefe de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3db66-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="3db66-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3db66-104">SYNTAX</span></span>

### <span data-ttu-id="3db66-105">Linux</span><span class="sxs-lookup"><span data-stu-id="3db66-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db66-106">Windows</span><span class="sxs-lookup"><span data-stu-id="3db66-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3db66-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3db66-107">DESCRIPTION</span></span>
<span data-ttu-id="3db66-108">O cmdlet **Remove-AzVMChefExtension** remove a extensão do Chefe de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3db66-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="3db66-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3db66-109">EXAMPLES</span></span>

### <span data-ttu-id="3db66-110">Exemplo 1: Remover uma extensão do Chefe de uma máquina virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="3db66-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="3db66-111">Este comando remove uma extensão do Chefe de uma máquina virtual baseada no Windows chamada WindowsVM001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="3db66-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="3db66-112">Exemplo 2: Remover uma extensão do Chefe de uma máquina virtual Linux</span><span class="sxs-lookup"><span data-stu-id="3db66-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="3db66-113">Este comando remove uma extensão do Chefe de uma máquina virtual baseada em Linux chamada LinuxVM001 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="3db66-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="3db66-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3db66-114">PARAMETERS</span></span>

### <span data-ttu-id="3db66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db66-115">-DefaultProfile</span></span>
<span data-ttu-id="3db66-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3db66-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3db66-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="3db66-117">-Linux</span></span>
<span data-ttu-id="3db66-118">Indica que esse cmdlet tem como destino uma máquina virtual Linux.</span><span class="sxs-lookup"><span data-stu-id="3db66-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db66-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3db66-119">-Name</span></span>
<span data-ttu-id="3db66-120">Especifica o nome da extensão do Chefe que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="3db66-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3db66-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3db66-121">-NoWait</span></span>
<span data-ttu-id="3db66-122">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="3db66-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3db66-123">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="3db66-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3db66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db66-124">-ResourceGroupName</span></span>
<span data-ttu-id="3db66-125">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3db66-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="3db66-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="3db66-126">-VMName</span></span>
<span data-ttu-id="3db66-127">Especifica o nome de uma máquina virtual para a qual este cmdlet remove a extensão do Chefe.</span><span class="sxs-lookup"><span data-stu-id="3db66-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="3db66-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="3db66-128">-Windows</span></span>
<span data-ttu-id="3db66-129">Indica que esse cmdlet se direciona a uma máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="3db66-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db66-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3db66-130">-Confirm</span></span>
<span data-ttu-id="3db66-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db66-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db66-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db66-132">-WhatIf</span></span>
<span data-ttu-id="3db66-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3db66-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db66-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3db66-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db66-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db66-135">CommonParameters</span></span>
<span data-ttu-id="3db66-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db66-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db66-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3db66-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db66-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3db66-138">INPUTS</span></span>

### <span data-ttu-id="3db66-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3db66-139">System.String</span></span>

## <span data-ttu-id="3db66-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3db66-140">OUTPUTS</span></span>

### <span data-ttu-id="3db66-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3db66-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3db66-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="3db66-142">NOTES</span></span>

## <span data-ttu-id="3db66-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3db66-143">RELATED LINKS</span></span>

[<span data-ttu-id="3db66-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3db66-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="3db66-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="3db66-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
