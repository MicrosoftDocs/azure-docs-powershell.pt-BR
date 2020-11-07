---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 888ba66f1949a687228f5b9f2563c3d810c7cd5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776923"
---
# <span data-ttu-id="1fd43-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1fd43-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="1fd43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fd43-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd43-103">Remove a extensão VMAccess de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fd43-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="1fd43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fd43-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fd43-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fd43-105">DESCRIPTION</span></span>
<span data-ttu-id="1fd43-106">O cmdlet **Remove-AzVMAccessExtension** remove a extensão da máquina virtual do VMAccess (acesso à máquina virtual) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fd43-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="1fd43-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fd43-107">EXAMPLES</span></span>

## <span data-ttu-id="1fd43-108">OS</span><span class="sxs-lookup"><span data-stu-id="1fd43-108">PARAMETERS</span></span>

### <span data-ttu-id="1fd43-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd43-109">-DefaultProfile</span></span>
<span data-ttu-id="1fd43-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd43-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd43-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1fd43-111">-Force</span></span>
<span data-ttu-id="1fd43-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1fd43-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd43-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fd43-113">-Name</span></span>
<span data-ttu-id="1fd43-114">Especifica o nome da extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1fd43-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd43-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd43-115">-ResourceGroupName</span></span>
<span data-ttu-id="1fd43-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fd43-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd43-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="1fd43-117">-VMName</span></span>
<span data-ttu-id="1fd43-118">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fd43-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1fd43-119">Esse cmdlet Remove VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1fd43-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fd43-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1fd43-120">-Confirm</span></span>
<span data-ttu-id="1fd43-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fd43-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd43-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd43-122">-WhatIf</span></span>
<span data-ttu-id="1fd43-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1fd43-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1fd43-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1fd43-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fd43-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd43-125">CommonParameters</span></span>
<span data-ttu-id="1fd43-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fd43-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd43-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd43-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd43-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fd43-128">INPUTS</span></span>

### <span data-ttu-id="1fd43-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1fd43-129">None</span></span>
<span data-ttu-id="1fd43-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1fd43-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1fd43-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fd43-131">OUTPUTS</span></span>

### <span data-ttu-id="1fd43-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1fd43-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1fd43-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fd43-133">NOTES</span></span>

## <span data-ttu-id="1fd43-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fd43-134">RELATED LINKS</span></span>

[<span data-ttu-id="1fd43-135">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1fd43-135">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="1fd43-136">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1fd43-136">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="1fd43-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1fd43-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
