---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: a409d4f6d09279aed6a22b9212894a1aca9cae1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771146"
---
# <span data-ttu-id="58f81-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="58f81-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="58f81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58f81-102">SYNOPSIS</span></span>
<span data-ttu-id="58f81-103">Remove a extensão VMAccess de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="58f81-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="58f81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58f81-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58f81-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58f81-105">DESCRIPTION</span></span>
<span data-ttu-id="58f81-106">O cmdlet **Remove-AzVMAccessExtension** remove a extensão da máquina virtual do VMAccess (acesso à máquina virtual) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="58f81-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="58f81-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58f81-107">EXAMPLES</span></span>

## <span data-ttu-id="58f81-108">OS</span><span class="sxs-lookup"><span data-stu-id="58f81-108">PARAMETERS</span></span>

### <span data-ttu-id="58f81-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f81-109">-DefaultProfile</span></span>
<span data-ttu-id="58f81-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58f81-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58f81-111">-Force</span><span class="sxs-lookup"><span data-stu-id="58f81-111">-Force</span></span>
<span data-ttu-id="58f81-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="58f81-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58f81-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="58f81-113">-Name</span></span>
<span data-ttu-id="58f81-114">Especifica o nome da extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="58f81-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="58f81-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58f81-115">-ResourceGroupName</span></span>
<span data-ttu-id="58f81-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="58f81-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="58f81-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="58f81-117">-VMName</span></span>
<span data-ttu-id="58f81-118">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="58f81-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="58f81-119">Esse cmdlet Remove VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="58f81-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="58f81-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58f81-120">-Confirm</span></span>
<span data-ttu-id="58f81-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58f81-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58f81-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f81-122">-WhatIf</span></span>
<span data-ttu-id="58f81-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58f81-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58f81-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58f81-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58f81-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f81-125">CommonParameters</span></span>
<span data-ttu-id="58f81-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f81-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f81-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58f81-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f81-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58f81-128">INPUTS</span></span>

### <span data-ttu-id="58f81-129">System. String</span><span class="sxs-lookup"><span data-stu-id="58f81-129">System.String</span></span>

## <span data-ttu-id="58f81-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58f81-130">OUTPUTS</span></span>

### <span data-ttu-id="58f81-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="58f81-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="58f81-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58f81-132">NOTES</span></span>

## <span data-ttu-id="58f81-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58f81-133">RELATED LINKS</span></span>

[<span data-ttu-id="58f81-134">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="58f81-134">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="58f81-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="58f81-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="58f81-136">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="58f81-136">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
