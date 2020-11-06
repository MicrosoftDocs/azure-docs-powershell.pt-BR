---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 53c9bc55c2ac8237544f293a4c42352d89681852
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597298"
---
# <span data-ttu-id="4e135-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="4e135-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="4e135-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e135-102">SYNOPSIS</span></span>
<span data-ttu-id="4e135-103">Remove uma extensão de script personalizada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4e135-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="4e135-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e135-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e135-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e135-105">DESCRIPTION</span></span>
<span data-ttu-id="4e135-106">O cmdlet **Remove-AzVMCustomScriptExtension** remove uma extensão de máquina virtual de script personalizada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4e135-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="4e135-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e135-107">EXAMPLES</span></span>

## <span data-ttu-id="4e135-108">OS</span><span class="sxs-lookup"><span data-stu-id="4e135-108">PARAMETERS</span></span>

### <span data-ttu-id="4e135-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e135-109">-DefaultProfile</span></span>
<span data-ttu-id="4e135-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e135-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e135-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4e135-111">-Force</span></span>
<span data-ttu-id="4e135-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4e135-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4e135-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e135-113">-Name</span></span>
<span data-ttu-id="4e135-114">Especifica o nome da extensão de script personalizada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="4e135-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4e135-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4e135-115">-NoWait</span></span>
<span data-ttu-id="4e135-116">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4e135-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4e135-117">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="4e135-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="4e135-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e135-118">-ResourceGroupName</span></span>
<span data-ttu-id="4e135-119">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4e135-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4e135-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="4e135-120">-VMName</span></span>
<span data-ttu-id="4e135-121">Especifica o nome de uma máquina virtual a partir da qual esse cmdlet Remove a extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="4e135-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="4e135-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4e135-122">-Confirm</span></span>
<span data-ttu-id="4e135-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e135-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e135-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e135-124">-WhatIf</span></span>
<span data-ttu-id="4e135-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4e135-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e135-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4e135-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e135-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e135-127">CommonParameters</span></span>
<span data-ttu-id="4e135-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e135-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e135-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e135-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e135-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e135-130">INPUTS</span></span>

### <span data-ttu-id="4e135-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4e135-131">System.String</span></span>

## <span data-ttu-id="4e135-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e135-132">OUTPUTS</span></span>

### <span data-ttu-id="4e135-133">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4e135-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4e135-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e135-134">NOTES</span></span>

## <span data-ttu-id="4e135-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e135-135">RELATED LINKS</span></span>

[<span data-ttu-id="4e135-136">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="4e135-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="4e135-137">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="4e135-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
