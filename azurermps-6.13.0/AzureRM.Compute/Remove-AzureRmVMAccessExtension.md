---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0360bcdb766de681ab6f54682007076e18266051
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602119"
---
# <span data-ttu-id="b9e9a-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b9e9a-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="b9e9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e9a-103">Remove a extensão VMAccess de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9e9a-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e9a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9e9a-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e9a-106">O cmdlet **Remove-AzureRmVMAccessExtension** remove a extensão da máquina virtual do VMAccess (acesso à máquina virtual) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="b9e9a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9e9a-107">EXAMPLES</span></span>

## <span data-ttu-id="b9e9a-108">OS</span><span class="sxs-lookup"><span data-stu-id="b9e9a-108">PARAMETERS</span></span>

### <span data-ttu-id="b9e9a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e9a-109">-DefaultProfile</span></span>
<span data-ttu-id="b9e9a-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e9a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b9e9a-111">-Force</span></span>
<span data-ttu-id="b9e9a-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9e9a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9e9a-113">-Name</span></span>
<span data-ttu-id="b9e9a-114">Especifica o nome da extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b9e9a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e9a-115">-ResourceGroupName</span></span>
<span data-ttu-id="b9e9a-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b9e9a-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="b9e9a-117">-VMName</span></span>
<span data-ttu-id="b9e9a-118">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b9e9a-119">Esse cmdlet Remove VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9e9a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9e9a-120">-Confirm</span></span>
<span data-ttu-id="b9e9a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e9a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e9a-122">-WhatIf</span></span>
<span data-ttu-id="b9e9a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e9a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e9a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e9a-125">CommonParameters</span></span>
<span data-ttu-id="b9e9a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e9a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e9a-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e9a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e9a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9e9a-128">INPUTS</span></span>

### <span data-ttu-id="b9e9a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b9e9a-129">System.String</span></span>

## <span data-ttu-id="b9e9a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9e9a-130">OUTPUTS</span></span>

### <span data-ttu-id="b9e9a-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b9e9a-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b9e9a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9e9a-132">NOTES</span></span>

## <span data-ttu-id="b9e9a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9e9a-133">RELATED LINKS</span></span>

[<span data-ttu-id="b9e9a-134">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b9e9a-134">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b9e9a-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b9e9a-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b9e9a-136">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="b9e9a-136">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
