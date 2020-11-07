---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942115"
---
# <span data-ttu-id="88378-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="88378-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="88378-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88378-102">SYNOPSIS</span></span>
<span data-ttu-id="88378-103">Remove a extensão chefe de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="88378-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="88378-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88378-104">SYNTAX</span></span>

### <span data-ttu-id="88378-105">Linux</span><span class="sxs-lookup"><span data-stu-id="88378-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88378-106">Windows</span><span class="sxs-lookup"><span data-stu-id="88378-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88378-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88378-107">DESCRIPTION</span></span>
<span data-ttu-id="88378-108">O cmdlet **Remove-AzVMChefExtension** remove a extensão chefe de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="88378-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="88378-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88378-109">EXAMPLES</span></span>

### <span data-ttu-id="88378-110">Exemplo 1: remover uma extensão chefe de um computador virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="88378-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="88378-111">Esse comando Remove uma extensão chefe de uma máquina virtual baseada em Windows nomeada WindowsVM001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="88378-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="88378-112">Exemplo 2: remover uma extensão chefe de um computador virtual Linux</span><span class="sxs-lookup"><span data-stu-id="88378-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="88378-113">Esse comando Remove uma extensão chefe de uma máquina virtual baseada em Linux nomeada LinuxVM001 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="88378-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="88378-114">OS</span><span class="sxs-lookup"><span data-stu-id="88378-114">PARAMETERS</span></span>

### <span data-ttu-id="88378-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88378-115">-DefaultProfile</span></span>
<span data-ttu-id="88378-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88378-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88378-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="88378-117">-Linux</span></span>
<span data-ttu-id="88378-118">Indica que esse cmdlet destina-se a um computador virtual Linux.</span><span class="sxs-lookup"><span data-stu-id="88378-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="88378-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="88378-119">-Name</span></span>
<span data-ttu-id="88378-120">Especifica o nome da extensão chefe que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="88378-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88378-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="88378-121">-NoWait</span></span>
<span data-ttu-id="88378-122">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="88378-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="88378-123">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="88378-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="88378-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88378-124">-ResourceGroupName</span></span>
<span data-ttu-id="88378-125">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="88378-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="88378-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="88378-126">-VMName</span></span>
<span data-ttu-id="88378-127">Especifica o nome de uma máquina virtual para a qual esse cmdlet Remove a extensão chefe.</span><span class="sxs-lookup"><span data-stu-id="88378-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="88378-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="88378-128">-Windows</span></span>
<span data-ttu-id="88378-129">Indica que esse cmdlet se destina a um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="88378-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="88378-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88378-130">-Confirm</span></span>
<span data-ttu-id="88378-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88378-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88378-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88378-132">-WhatIf</span></span>
<span data-ttu-id="88378-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88378-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88378-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88378-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88378-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88378-135">CommonParameters</span></span>
<span data-ttu-id="88378-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88378-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88378-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88378-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88378-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88378-138">INPUTS</span></span>

### <span data-ttu-id="88378-139">System. String</span><span class="sxs-lookup"><span data-stu-id="88378-139">System.String</span></span>

## <span data-ttu-id="88378-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88378-140">OUTPUTS</span></span>

### <span data-ttu-id="88378-141">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="88378-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="88378-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88378-142">NOTES</span></span>

## <span data-ttu-id="88378-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88378-143">RELATED LINKS</span></span>

[<span data-ttu-id="88378-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="88378-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="88378-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="88378-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
