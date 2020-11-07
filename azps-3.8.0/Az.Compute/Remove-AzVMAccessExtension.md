---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 6c02a8381ca1cda4fec6fb52ea3d798884b45bad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942112"
---
# <span data-ttu-id="1271b-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1271b-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="1271b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1271b-102">SYNOPSIS</span></span>
<span data-ttu-id="1271b-103">Remove a extensão VMAccess de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1271b-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="1271b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1271b-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1271b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1271b-105">DESCRIPTION</span></span>
<span data-ttu-id="1271b-106">O cmdlet **Remove-AzVMAccessExtension** remove a extensão da máquina virtual do VMAccess (acesso à máquina virtual) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1271b-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="1271b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1271b-107">EXAMPLES</span></span>

## <span data-ttu-id="1271b-108">OS</span><span class="sxs-lookup"><span data-stu-id="1271b-108">PARAMETERS</span></span>

### <span data-ttu-id="1271b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1271b-109">-DefaultProfile</span></span>
<span data-ttu-id="1271b-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1271b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1271b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1271b-111">-Force</span></span>
<span data-ttu-id="1271b-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1271b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1271b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1271b-113">-Name</span></span>
<span data-ttu-id="1271b-114">Especifica o nome da extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1271b-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1271b-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1271b-115">-NoWait</span></span>
<span data-ttu-id="1271b-116">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="1271b-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1271b-117">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="1271b-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1271b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1271b-118">-ResourceGroupName</span></span>
<span data-ttu-id="1271b-119">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1271b-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1271b-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="1271b-120">-VMName</span></span>
<span data-ttu-id="1271b-121">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1271b-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1271b-122">Esse cmdlet Remove VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1271b-122">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1271b-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1271b-123">-Confirm</span></span>
<span data-ttu-id="1271b-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1271b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1271b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1271b-125">-WhatIf</span></span>
<span data-ttu-id="1271b-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1271b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1271b-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1271b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1271b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1271b-128">CommonParameters</span></span>
<span data-ttu-id="1271b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1271b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1271b-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1271b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1271b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1271b-131">INPUTS</span></span>

### <span data-ttu-id="1271b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1271b-132">System.String</span></span>

## <span data-ttu-id="1271b-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1271b-133">OUTPUTS</span></span>

### <span data-ttu-id="1271b-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1271b-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1271b-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1271b-135">NOTES</span></span>

## <span data-ttu-id="1271b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1271b-136">RELATED LINKS</span></span>

[<span data-ttu-id="1271b-137">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1271b-137">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="1271b-138">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1271b-138">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="1271b-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1271b-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
